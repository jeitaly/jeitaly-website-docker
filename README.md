# WordPress Local Development with Docker

This repository provides an easy way for university students to set up a local WordPress environment using Docker and Docker Compose. This allows you to develop and test your WordPress projects without any costs or complex configurations.

This project has been created by the IT department of JE Italy, the Italian Confederation of Junior Enterprises.

## Prerequisites

Before running this setup, ensure you have the following installed on your system:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. **Clone the Repository**
   ```sh
   git clone https://github.com/jeitaly/jeitaly-website-docker.git
   cd jeitaly-website-docker
   ```

2. **Start the Containers**
   ```sh
   docker compose up -d
   ```
   This command will:
   - Start an Apache server with PHP and WordPress installed.
   - Start a MySQL database.

3. **Access Your Local WordPress Site**
   - Open your browser and navigate to: [http://localhost:8080](http://localhost:8080)
   - Follow the WordPress installation process.
   - Use the following database settings during setup:
     - **Database Name**: `wordpress`
     - **Username**: `wordpress`
     - **Password**: `oe%hiuth8Aghub5ein8a`
     - **Database Host**: `mysql`

## Stopping the Environment

To stop the containers, run:
```sh
docker compose down
```

## Persistent Data

- Your website files are stored in the `website/` directory.
- Your MySQL data is stored in the `mysql_data` volume.

## Troubleshooting

- If port 8080 is in use, modify the `docker compose.yml` file and change `127.0.0.1:8080:80` to another port.
- If you experience database connection issues, ensure MySQL is running and check the container logs:
  ```sh
  docker logs mysql
  ```

## Contributing

This repository is created for university students to facilitate WordPress development. Feel free to fork and modify it according to your needs.

## License

This project is open-source and free to use for educational purposes.


