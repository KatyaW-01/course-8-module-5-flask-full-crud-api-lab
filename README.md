# Flask CRUD API Lab

This project is a simple RESTful API built using **Python** and **Flask**. It demonstrates how to implement full **CRUD operations**—specifically, **POST**, **PATCH**, and **DELETE**—to manage a list of events in an in-memory data structure.

## Lab Objective

The lab reinforces key backend development concepts:

- Handling HTTP methods (`POST`, `PATCH`, `DELETE`)
- Designing RESTful routes
- Processing incoming JSON data with `request.get_json()`
- Simulating database behavior with in-memory Python objects
- Formatting and returning responses in JSON

## Technologies Used

- Python 3
- Flask

## Getting Started

### Installation

1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
2. (Optional) Create and activate a virtual environment:
    ```bash
    virtualenv env
    source env/bin/activate 
    ```
3. Install Flask
    ```bash
    pip install Flask
    ```
## API Endpoints

### Create an Event

**Endpoint**: `POST /events`  
**Description**: Create a new event using JSON input.

**Request Body**:
```json
{
  "title": "New Event Title"
}
```
**Response**:
- `201 Created`
- Returns the created event in the Json format:
  ```json
  {
  "id": 3,
  "title": "New Event Title"
  }
  ```
### Update an Event

**Endpoint**: `PATCH /events/<event_id>` <br>
**Description**: Update the title of an existing event by ID.

**Request Body**:
```json
{
  "title": "Updated Title"
}
```

**Response**:
- `200 OK` - if the event exists, returns the updated event:
  ```json
  {
    "id": 2,
    "title": "Updated Title"
  }
  ```
- `404 Not Found` - if the event ID does not exist

### Delete an Event

**Endpoint**: `DELETE /events/<event_id>` <br>
**Description**: Delete an event by its ID.

**Response**:
- `204 No Content` - if the event was deleted successfully
- `404 Not Found` - if the event ID does not exist






