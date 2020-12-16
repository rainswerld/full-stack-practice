# Full Stack Project Practice

Be prepared to discuss these items with a consultant during a 1 on 1.

You may use GitHub, PowerPoint, Keynote, or any other tools you desire to
complete any part of this.

## Project Idea

What is your project idea?  How did you come up with it? Why? Who would use it?

```md
My project idea is to create a fermented drink recipe guide called Effervess. I love fermentation, escpecially fermented drinks lilke kombucha, kefir, and beer. I haven't found a website that has a nice UI that has useful recipes for different types of fermentable drinks - especially not one that has kombucha, kefir, and beer all in one.

Since I have experience brewing all three types of fermented drinks, I will be able to get started with a database of recipes for various types of kombucha, kefir, and beer.

Additionally, a user will be able to create, store, update, and delete their recipes with this fermented drink application.
```

## Write between 3-5 user stories

We have gone over this before. Please refer to your notes, previous repos or the
google machine if you need further assistance.

```md
1. As a user, I would like to signup, signin, logout, and change my password.
2. As a user, I would like to see other people's recipes for kombucha, beer, and kefir.
3. As a user, I would like to create, store, update, and delete my own recipes.
4. As a user, I would like to see all the recipes I've created.
```

## Wireframes

Please create a wireframe of your planned front end.

```md
https://imgur.com/EtB32SF
https://imgur.com/u5s18y0
https://imgur.com/BV8zwvh
```

## Plan your resources

What resources will you need? What will the attributes and relationships be?

```md
I will need a authentication/user resource that stores information about users (username, password).
The user resource will be something like:
user: {
  username: examplename,
  password: examplepassword,
  recipes: [
    {
      recipe1: {
        name: 'Strawberry booch',
        type: kombucha,
        ingredients: ['4 lbs strawberrys', 'Mama scoby'],
        instructions: ['Do this', 'then do that']
        owner: examplename
        }
      recipe2: {
        name: 'Simple IPA',
        type: beer,
        ingredients: ['Malt', 'Hops', 'Yeast'],
        instructions: ['Do this', 'then do that']
        owner: examplename
      }
    }
  ]
}

I the user instance, the user will "own" recipes.

Additionally, I will need a resource that stores the "application's" recipes - or the recipes that everyone can see.

The relationship between user and recipe will be one to many - there is one user with many recipes. There is only one user for many recipes is another way to look at that.
```

## Create an ERD (entity relationship diagram)

These are the diagrams that show how your resources are related to one another
(one to many, many to many, etc).

Include an image (or a link to image) below.

```md
https://imgur.com/xzp5WaZ
```

## Routing

What routes will you need to make the proper request to your API?

```md
/user/:id
/user/:id/recipes
/user/:id/recipes/:id

When the application takes on different types of recipes (will start with beer recipes, then add kombucha and kefir) the routes would look more like:
/user/:id/recipes/beer/:id
/user/:id/recipes/kombucha/:id
/user/:id/recipes/kefir/:id
/user/:id/recipes
```

## Timetable

Write a basic timetable for yourself, you don't have to stick to it but it
helps to go in with a plan.

```md
I've used this as reference: https://git.generalassemb.ly/ga-wdi-boston/full-stack-project/blob/master/schedule.md


Day 1:
- Planning
- API Setup
- Client Setup

Day 2:
- API

Day 3:
- Client

Day 4:
- Final touches
```
