# Recipe Generation using Recurrent Neural Networks (RNN)

## Overview

In this experiment, I use character-based Recurrent Neural Networks (RNN) to generate cooking recipes. The goal is to train the RNN to generate recipe names, ingredients, and cooking instructions. I used three models (Simple RNN, LSTM, GRU) with two different optimizers (Adaptive Moment Estimation (ADAM) & Nesterov-accelerated Adaptive Moment Estimation (NADAM)). The experiment utilizes TensorFlow v2 with its Keras API.

## Dataset

The dataset can be downloaded from [here](https://eightportions.com/datasets/Recipes/). It consists of approximately 125,000 recipes scraped from various food websites. Each recipe includes:

- **Title**: The name of the recipe, e.g., "Guacamole".
- **Ingredients**: A detailed list of all required ingredients, including measurements.
- **Instructions**: Step-by-step directions on how to prepare the dish.

Each recipe is stored in JSON format with keys for the title, ingredients, and instructions. Example JSON:

```json
{
    "title": "Guacamole",
    "ingredients": [
        "3 Haas avocados, halved, seeded and peeled",
        "1 lime, juiced",
        "1/2 teaspoon kosher salt",
        "1/2 teaspoon ground cumin",
        "1/2 teaspoon cayenne",
        "1/2 medium onion, diced",
        "1/2 jalapeño pepper, seeded and minced",
        "2 Roma tomatoes, seeded and diced",
        "1 tablespoon chopped cilantro",
        "1 clove garlic, minced"
    ],
    "instructions": "In a large bowl place the scooped avocado pulp and lime juice, toss to coat. Drain, and reserve the lime juice, after all of the avocados have been coated. Using a potato masher add the salt, cumin, and cayenne and mash. Then, fold in the onions, tomatoes, cilantro, and garlic. Add 1 tablespoon of the reserved lime juice. Let sit at room temperature for 1 hour and then serve."
}
