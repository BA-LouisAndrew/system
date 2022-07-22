## Prerequisites

Docker is installed and accessible via the terminal

## Running

To run the system, please run: the following command in your terminal

```
docker-compose up -d --build
```

Please keep in mind that it takes a while until the RabbitMQ instance is ready to be used. Before the RabbitMQ instance is ready, the FDS won't be accessible.

## Message Consumer

The message consumer source code is accessible within the `services` folder. Some environment variables need to be configured to set up the program properly, preferably via a `.env` file:
- MAIL_SERVER: email server to send the email
- MAIL_USER: user to log in to the mail server
- MAIL_PASS: password to log in
- MAIL_DISPLAY_NAME: display name of the sender
- MAIL_ADDRESS: email address of the sender
- FRONTEND_URL: URL to the UI of the system, used to link to the corresponding validation process
- RABBITMQ_URL: URI to the RabbitMQ instance

To run the message consumer, please make sure that the environment variables are present and run the following command in your terminal:

```
npm start
```
