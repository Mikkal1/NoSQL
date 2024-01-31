# 18 NoSQL: Social Network API

## Table of Contents

1. [Description](#description)
2. [Walkthrough Video](#walkthrough-video)
3. [Installation](#installation)
4. [API Usage](#api-usage)

## Description

This project is an API for a social network web application where users can share their thoughts, react to friends' thoughts, and create a friend list. It uses Express.js for routing, a MongoDB database, and the Mongoose ODM.

## Walkthrough Videos

## Installation

Follow the steps below to run the application on your local machine after downloading the repository:

```bash
    npm install
    npm start
```

You can then use an API platform like Insomia to test.

## API Usage

This application provides several API endpoints for managing users, their friends, thoughts, and reactions. Here's how you can use them:

### User Endpoints

- `POST /api/users` - Create a new user. The request body should include `username` and `email`.

- `GET /api/users` - Get a list of all users.

- `GET /api/users/:userId` - Get a specific user by their `_id`.

- `PUT /api/users/:userId` - Update a user by their `_id`. The request body should include the fields you want to update.

- `DELETE /api/users/:userId` - Delete a user by their `_id`.

### Friend Endpoints

- `POST /api/users/:userId/friends/:friendId` - Add a new friend to a user's friend list.

- `DELETE /api/users/:userId/friends/:friendId` - Remove a friend from a user's friend list.

### Thought Endpoints

- `GET /api/thoughts` - Get all thoughts.

- `POST /api/thoughts` - Create a new thought. The request body should include `thoughtText`, `username`, and `userId`.

- `GET /api/thoughts/:thoughtId` - Get a single thought by its `_id`.

- `PUT /api/thoughts/:thoughtId` - Update a thought by its `_id`. The request body should include the fields you want to update.

- `DELETE /api/thoughts/:thoughtId` - Remove a thought by its `_id`.

### Reaction Endpoints

- `POST /api/thoughts/:thoughtId/reactions` - Create a reaction. The request body should include `reactionBody` and `username`.

Remember to replace `:userId`, `:friendId`, and `:thoughtId` with actual IDs when making requests.
