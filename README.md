# Asg1
A basic todo-list api


API Documentation

Overview--------

This API is a RESTful API for a To-Do list application. It allows users to create, read, update, and delete To-Do list items.

Endpoints--------

The API has the following endpoints:

/todo-items: This endpoint returns a list of all To-Do list items.
/todo-items/:id: This endpoint returns a single To-Do list item by its ID.
/todo-items: This endpoint creates a new To-Do list item.
/todo-items/:id: This endpoint updates a To-Do list item.
/todo-items/:id: This endpoint deletes a To-Do list item.

Request and Response Bodies----------

The request and response bodies are JSON objects. The request body for the /todo-items endpoint must contain the following fields:
The response body for the /todo-items endpoint is an array of To-Do list items. Each To-Do list item object has the following fields:

id: The ID of the To-Do list item.
title: The title of the To-Do list item.
description: The description of the To-Do list item.
completed: A boolean value indicating whether the To-Do list item has been completed.
due_date: The due date for the To-Do list item.
priority: The priority of the To-Do list item.

The following is the database schema for a To-Do list application:

SQL
CREATE SCHEMA todo_list;

CREATE TABLE todo_list.todo_items (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  description TEXT,
  completed BOOLEAN NOT NULL DEFAULT FALSE,
  due_date DATE,
  priority INTEGER
);
