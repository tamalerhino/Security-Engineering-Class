# Overview

Learn what an API is, how to make API calls using curl , and explore different endpoints to gather information on various Pokémon. You will also learn how to interpret JSON responses and experiment with more advanced API features.

## What is an API?

Imagine you’re at a restaurant. You have a menu with all the food you can order, but you can't go into the kitchen to make it yourself. Instead, you tell the waiter what you want, and they go to the kitchen, get the food, and bring it back to you.

An **API** is like that waiter. It’s a helper that takes your order (your request for information or action) and goes to a “kitchen” (the service or database) to get what you asked for. Then it brings the answer back to you.

So, when we use an API, we’re asking a helper (the API) to go get information or perform an action for us from another place—like getting information about a Pokémon from the Pokémon kitchen!

In summary an **API (Application Programming Interface)** allows different applications to communicate with each other. With APIs, you can request data, send data, and interact with other applications or services over the internet. In this exercise, we will use the Pokémon API to explore the concept.

## Making Your First API Call with cURL
### Fetch Basic Pokémon Information

Open your terminal(or VM) and try this basic command with curl to get information about a specific Pokémon. Let's start with Pikachu.
```bash
curl -s https://pokeapi.co/api/v2/pokemon/pikachu
```
**What You Should See:**

- A JSON response with details about Pikachu.
- You’ll see Pikachu’s **name, id, height, weight, types** (like “electric”), and **abilities** (like “static”).
- This JSON structure is hierarchical, meaning some information (like abilities) is nested inside other objects.

### Exploring the JSON Response

JSON format can be hard to read in the terminal, so you can use the jq tool (or pipe to python -m json.tool - if you dont have jq installed) to make it more readable.
```bash
curl -s https://pokeapi.co/api/v2/pokemon/pikachu | jq
```

**What You Should See:**
- A nicely formatted JSON response.
- You can see nested sections more clearly now, making it easier to understand Pikachu’s data.
## Querying Different Endpoints

Now, we’ll explore various Pokémon API endpoints to learn how to retrieve different types of data.

### Pokémon Species Information

This endpoint shows broader species information about Pikachu, not just individual stats.
```bash
curl -s https://pokeapi.co/api/v2/pokemon-species/pikachu | jq
```

**What You Should See:** 

- Data on Pikachu’s habitat and flavor text (description).
- Information on whether Pikachu has alternate forms or evolutions.
- Extra details like color and shape, which can be used to classify Pokémon.

### List of Pokémon Types

The API can give you a list of all Pokémon types, like fire, water, grass, etc.
```bash
curl -s https://pokeapi.co/api/v2/type | jq
```
**What You Should See:**

- A list of Pokémon types with URLs for each.
- Each type links to more information about it, so you can look up specific types to see which Pokémon belong to them.

### Viewing Details of a Specific Type

Let’s use one of the types from the list to get more detailed information. For instance, the "fire" type:
```bash
curl -s https://pokeapi.co/api/v2/type/fire | jq
```

**What You Should See:**

- A list of Pokémon that belong to the fire type.
- You’ll also see **damage relations**, which show what types are strong or weak against fire.

### Explore Pokémon Abilities

Let’s look into Pikachu’s abilities. When we queried the `/pokemon/pikachu` endpoint, you saw Pikachu’s abilities listed there. Each ability comes with a URL to get more information.
```bash
curl -s https://pokeapi.co/api/v2/ability/31 | jq
```

**What You Should See:**

- Detailed information about the ability, like a **description** of what it does and which Pokémon can have it.
- Some abilities are “hidden” abilities, which are rarer.

### Evolution Chains

Most Pokémon have evolution chains. The evolution chain for Pikachu, for example, includes Pichu and Raichu.
```bash
curl -s https://pokeapi.co/api/v2/evolution-chain/10/ | jq
```

**What You Should See:**

- Information about Pikachu’s evolution stages, such as how Pikachu evolves from Pichu and can evolve into Raichu.
- Conditions for evolution, like needing a certain level or an item.

### Random Pokémon Generator

Fetching a random Pokémon involves generating a random ID. Run this command to see information on a random Pokémon each time.
```bash
RANDOM_ID=$((1 + RANDOM % 898))
curl -s "https://pokeapi.co/api/v2/pokemon/$RANDOM_ID" | jq
```

**What You Should See:**

- Each time you run it, you’ll get a different Pokémon with its name, height, weight, and other details.
- You can combine this with a small script to fetch several random Pokémon at once.

### List All Moves for a Pokémon

Pokémon can learn various moves. Let’s take a look at the moves Charizard can learn.
```bash
curl -s https://pokeapi.co/api/v2/pokemon/charizard | jq
```
**What You Should See:**

- A list of moves Charizard can learn, with details on when and how the moves are learned.
- Moves have different methods of learning (e.g., through leveling up, machines, or tutors).

## Filtering Basic Info

Hitting API's is great and all but ideally you would only want one or two things from entire results. Here is how we can use jq to filter for only specific attributes within the response.

### Fetch Basic Pokémon Information and Filter for Specific Attributes

Let’s start by fetching data for Pikachu and using jq to filter specific attributes. Try running this command:
```bash
curl -s https://pokeapi.co/api/v2/pokemon/pikachu | jq '.name, .height, .weight'
```

**What You Should See:**

- Only Pikachu’s name, height, and weight displayed in the terminal in that order.
- This command helps you focus on specific details within a larger JSON response.

### Extracting Types Using jq
Next, we’ll fetch the types for Pikachu. In the JSON response, types are nested within an array, so let’s use jq to filter them.
```bash
curl -s https://pokeapi.co/api/v2/pokemon/pikachu | jq '.types[].type.name'
```

**What You Should See:**

- Only the names of Pikachu’s types (e.g., "electric").
- The `.types[].type.name` syntax drills down through the nested structure to find the type names.

### Finding Abilities Using jq

Use `jq` to list all abilities of Pikachu. Here’s the command:
```bash
curl -s https://pokeapi.co/api/v2/pokemon/pikachu | jq '.abilities[].ability.name'
```
**What You Should See:**

- The names of Pikachu’s abilities (like "static" and possibly a hidden ability if present).
- This focuses specifically on ability names, skipping other attributes.

## Using jq to Filter on Complex Data

Now that you’re familiar with basic filtering, let’s try more advanced filtering.

### Filtering Moves by Learning Method

Pokémon learn moves in different ways, such as by leveling up or using items. Let’s focus on moves Pikachu can learn via leveling up.
```bash
curl -s https://pokeapi.co/api/v2/pokemon/pikachu | jq '.moves[] | select(.version_group_details[].move_learn_method.name == "level-up") | .move.name'
```

**What You Should See:**

- A list of moves Pikachu learns through leveling up.
- The select function in jq filters moves based on the move_learn_method attribute.

### Finding Pokémon Weaknesses by Type

Let’s look at weaknesses for the fire type by accessing the damage relations.
```bash
curl -s https://pokeapi.co/api/v2/type/fire | jq '.damage_relations.double_damage_from[].name'
```

**What You Should See:**

- A list of types that do double damage to fire-type Pokémon.
- This shows only the type names that fire-type Pokémon are weak against.

### Using jq to Format Output as a Table

For a more structured output, try printing name and height/weight of Pikachu in a simple format:
```bash
curl -s "https://pokeapi.co/api/v2/pokemon/pikachu" | jq '{Name: .name, Height: .height, Weight: .weight}'
```

**What You Should See:**

- The Pokémon’s name, height, and weight in a structured JSON format.
- This approach lets you create a customized view of the data.

## Summary

With these exercises, you should now:

Understand what an API is and how to interact with it using curl.
Be able to explore and interpret JSON responses.
Filtering those responses using jq
Know how to use nested JSON objects to find more specific information.
Feel comfortable navigating various endpoints in the Pokémon API.