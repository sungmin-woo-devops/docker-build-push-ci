# Multi-Environment Docker Images

This repository contains Dockerfiles and resources for building and pushing Docker images for various web servers across different Linux distributions. The repository is structured to easily manage multiple Docker images, including configurations for both Nginx and Apache on Alpine and Ubuntu.

## Repository Structure

```plaintext
my-github-repo/
├── docker/
│   ├── alpine-nginx/
│   │   ├── Dockerfile.alpine-nginx
│   │   └── index.html
│   ├── ubuntu-nginx/
│   │   ├── Dockerfile.ubuntu-nginx
│   │   └── nginx.conf
│   ├── alpine-apache/
│   │   ├── Dockerfile.alpine-apache
│   │   └── httpd.conf
│   └── ubuntu-apache/
│       ├── Dockerfile.ubuntu-apache
│       └── httpd.conf
├── .github/
│   └── workflows/
│       ├── build-and-push-alpine-nginx.yml
│       ├── build-and-push-ubuntu-nginx.yml
│       ├── build-and-push-alpine-apache.yml
│       └── build-and-push-ubuntu-apache.yml
└── README.md
```

## Docker Images

### 1. Alpine Nginx
- **Path**: `docker/alpine-nginx/`
- **Dockerfile**: `Dockerfile.alpine-nginx`
- **Description**: This image builds Nginx on Alpine Linux, optimized for lightweight environments. The `index.html` file is used as the default homepage.

### 2. Ubuntu Nginx
- **Path**: `docker/ubuntu-nginx/`
- **Dockerfile**: `Dockerfile.ubuntu-nginx`
- **Description**: This image builds Nginx on Ubuntu, providing a more feature-rich environment. The `nginx.conf` file is used to configure Nginx settings.

### 3. Alpine Apache
- **Path**: `docker/alpine-apache/`
- **Dockerfile**: `Dockerfile.alpine-apache`
- **Description**: This image builds Apache HTTP Server on Alpine Linux, ideal for lightweight web server setups. The `httpd.conf` file is used to configure Apache settings.

### 4. Ubuntu Apache
- **Path**: `docker/ubuntu-apache/`
- **Dockerfile**: `Dockerfile.ubuntu-apache`
- **Description**: This image builds Apache HTTP Server on Ubuntu, suitable for environments requiring robust and extensive features. The `httpd.conf` file is used for server configuration.

## GitHub Actions Workflows

This repository includes several GitHub Actions workflows that automate the building and pushing of Docker images to Docker Hub. Each workflow corresponds to a specific Dockerfile and is triggered on a push to the `main` branch.

- **Build and Push Alpine Nginx**: `.github/workflows/build-and-push-alpine-nginx.yml`
- **Build and Push Ubuntu Nginx**: `.github/workflows/build-and-push-ubuntu-nginx.yml`
- **Build and Push Alpine Apache**: `.github/workflows/build-and-push-alpine-apache.yml`
- **Build and Push Ubuntu Apache**: `.github/workflows/build-and-push-ubuntu-apache.yml`

## Usage

To build and push any of the Docker images:

1. Push your changes to the `main` branch of this repository.
2. The corresponding GitHub Actions workflow will be triggered automatically.
3. The Docker image will be built using the specified Dockerfile and then pushed to Docker Hub under your account.

## Adding a New Dockerfile

To add a new Dockerfile and workflow:

1. Create a new directory under `docker/` with a descriptive name (e.g., `docker/centos-nginx/`).
2. Add your Dockerfile and any necessary resources to this directory.
3. Create a new GitHub Actions workflow file under `.github/workflows/` to build and push your image.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your changes. Make sure to follow the existing code style and include relevant documentation.

## Contact

For any inquiries, please contact [Your Name](mailto:your.email@example.com).
