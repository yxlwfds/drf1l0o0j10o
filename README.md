## Prerequisites

Before using this template, ensure that you have the following dependencies installed on your system:

- Docker: [Install Docker](https://www.docker.com/get-started)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

To start a new project using this template, follow these steps:

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yxlwfds/drf1l0o0j10o1.git
```

2. Navigate into the `myproject` directory:

```bash
cd myproject
```

Open the `.env` file and set the value of all environment variables.

3. Build and run the Docker containers:

```bash
docker-compose up -d --build
```

This command will download the required Docker images, set up the containers, and start the development server.

5. Access the Django application:

You can access the Django application running on `127.0.0.1:8000` in your web browser.

6. Test the API endpoint:

- `/signup/`, testing request:

    ```bash
    curl --location 'http://127.0.0.1:8000/signup/' --data-raw '{"email": "test@test.com","password": "123"}'
    ```

    - Expected server response: {id, email} of the user
- `/signin/` , testing request:

    ```bash
    curl --location http://127.0.0.1:8000/signin/ --data-raw '{"email": "test@test.com","password": "123"}'
    ```

    - Expected server response: dict of {access_token, refresh_token}
- `/me/`, testing request:

    ```bash
    curl --location 'http://127.0.0.1:8000/me/' --header 'Authorization: Bearer <eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNzE2OTc1Nzg1LCJpYXQiOjE3MTY5NzM5ODUsImp0aSI6ImJhMmNlODQ2ODY1NjRkYmNhMDk0YjAwOTg5NTBlZWFkIiwidXNlcl9pZCI6MX0.ULM83py1CkMS2lovi-3fOEkZ8NRjijYt-dQXQXJlBxo'
