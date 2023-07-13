# Django Rest Framework API

This is a simple Django Rest Framework API that allows you to manage drinks.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/saa1man/django-rest-api
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Apply the database migrations:

```bash
python manage.py migrate
```

4. Start the development server:

```bash
python manage.py runserver
```

## API Endpoints

### Drinks

- `GET /drinks/`: Get a list of all drinks.
- `POST /drinks/`: Create a new drink.

- `GET /drinks/<int:id>/`: Get details of a specific drink.
- `PUT /drinks/<int:id>/`: Update details of a specific drink.
- `DELETE /drinks/<int:id>/`: Delete a specific drink.

## Usage

### Get a list of all drinks

**Request:**

```http
GET /drinks/
```

**Response:**

```json
[
    {
        "id": 1,
        "name": "Coffee",
        "description": "A hot and energizing beverage"
    },
    {
        "id": 2,
        "name": "Tea",
        "description": "A refreshing and aromatic drink"
    },
    ...
]
```

### Create a new drink

**Request:**

```http
POST /drinks/
Content-Type: application/json

{
    "name": "Orange Juice",
    "description": "A tangy and citrusy drink"
}
```

**Response:**

```json
{
    "id": 3,
    "name": "Orange Juice",
    "description": "A tangy and citrusy drink"
}
```

### Get details of a specific drink

**Request:**

```http
GET /drinks/1/
```

**Response:**

```json
{
    "id": 1,
    "name": "Coffee",
    "description": "A hot and energizing beverage"
}
```

### Update details of a specific drink

**Request:**

```http
PUT /drinks/1/
Content-Type: application/json

{
    "name": "Espresso",
    "description": "A concentrated form of coffee"
}
```

**Response:**

```json
{
    "id": 1,
    "name": "Espresso",
    "description": "A concentrated form of coffee"
}
```

### Delete a specific drink

**Request:**

```http
DELETE /drinks/1/
```

**Response:**

```
No content. The drink has been deleted successfully.
```
