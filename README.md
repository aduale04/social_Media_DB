# Social Media Application Database Design

## Overview

This document outlines the relational database model for a social media application. The model includes the following entities: User, Friends, Post, Comment, Reacts.

## Entities and Attributes

### User
The User entity represents an individual user of the social media application. It includes the following attributes:

- User ID: A unique identifier for each user.
- Name: The user's name.
- Age: The user's age.
- Gender: The user's gender.
- Profile Picture: A reference to the user's profile picture.
- Address: The user's address.

### Friends
The Friends entity represents the relationships between users, indicating which users are friends with one another. It includes the following attributes:

- User ID: A reference to the user who is a friend.
- Friend ID: A reference to the user's friend.

### Post
The Post entity represents a post made by a user. It includes the following attributes:

- Post ID: A unique identifier for each post.
- User ID: A reference to the user who made the post.
- Content: The post's content.
- Date: The date the post was made.
- Image(s): A reference to any images associated with the post.

### Comment
The Comment entity represents a comment made by a user in response to a post. It includes the following attributes:

- Comment ID: A unique identifier for each comment.
- User ID: A reference to the user who made the comment.
- Post ID: A reference to the post the comment is in response to.
- Content: The comment's content.
- Date: The date the comment was made.
- Image(s): A reference to any images associated with the comment.

### Reacts
The Reacts entity represents a reaction made by a user in response to a post or comment. It includes the following attributes:

- React ID: A unique identifier for each reaction.
- User ID: A reference to the user who made the reaction.
- Post/Comment ID: A reference to the post or comment the reaction is in response to.
- Type: The type of reaction made.

## Relationships

The entities are related to one another through relationships, allowing for the efficient storage and retrieval of data for the social media application. The relationships between the entities are as follows:

- A User can have multiple Posts (one-to-many relationship).
- A User can have multiple Comments (one-to-many relationship).
- A User can have multiple Reacts (one-to-many relationship).
- A User can have multiple Friends (many-to-many relationship).
- A Post can have multiple Comments (one-to-many relationship).
- A Post can have multiple Reacts (one-to-many relationship).
- A Comment can have multiple Reacts (one-to-many relationship).

## Database Design Image

[https://github.com/aduale04/social_Media_DB/blob/bbb6a5445fe3fe9595f16eaa0acb0c0024c422e0/Social%20Media%20Database%20ER%20diagram.jpeg]
