# Project

Ask: Create a new app/api + endpoint to "get meals using the main ingredient" using the https://www.themealdb.com/api.php.

Input: ingredient
Output: list of meals that use inputted ingredient

Meal Object

```ts
class Meal {
  id: number;
  name: string;
  instructions: string;
  tags: string[];
  thumbUrl: string;
  youtubeUrl: string;
  ingredients: { ingredient: string; measurement: string }[];
}
```

Example Meal Object:

```ts
{
    id: 52820,
    name: 'Katsu Chicken curry',
    instructions: 'Prep:15min \u203a Cook:30min \u203a Ready in:...’,
    tags: ['Curry', 'Meat'],
    thumbUrl: 'https://www.themealdb.com/images/media/meals/vwrpps1503068729.jpg',
    youtubeUrl: 'https://www.youtube.com/watch?v=MWzxDFRtVbc',
    ingredients: [
        {
            ingredient: 'chicken breast',
            measurement: '4 pounded to 1cm thickness'
        },
        {
            ingredient: 'plain flour',
            measurement: '2 tablespoons'
        },
    ...
    ]
}
```

How to run:

1. navigate to root directory
2. npm install
3. npm start
4. open http://localhost:3000/<ingredient_of_choice>

Overview

- Communicates with / backed-by MealsDB
- Request parameter is a “string” that represents the main ingredient, e.g. “chicken”
- Response is an array of “Meal”s - specified below, with initial values as examples
- Tech: Node / Express / Typescript (anything beyond that is welcome!)
- Testable via Postman
- Used API rate limiting
