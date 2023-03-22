# Penzle.Self-Hosted
The Self-Hosted edition of Penzle run on a server or computer that is owned and maintained by the user. This means that the you have complete control over the software and data, including customization, privacy, and security. 

## Getting started
This repository contains a docker-compose file for the Penzle project, which consists of the following services:

- **Email**: An SMTP service for testing and sending emails.
- **SQL Server**: A free Microsoft SQL Server instance based on Linux.
- **Azure Storage**: An Azurite instance for emulating Azure Blob Storage.
- **Seq**: A Seq instance for log management and analysis.
- **Web**: The Penzle Web Application.
- **Penzle API**: The Penzle API service.

## Prerequisites
To run this project, you need to have Docker installed on your system. You can download Docker Desktop for Windows, macOS, or Linux from the following link: https://www.docker.com/products/docker-desktop

## How to Run
To run the Penzle project using the provided docker-compose file, follow these steps for your operating system:

### Windows
- Open a Command Prompt or PowerShell window.
- Navigate to the folder containing the docker-compose file.
- Run the following command:

```
docker-compose -f .\docker-compose-self-hosting.yaml -p penzle-environment up -d
```

### Linux
- Open a terminal window.
- Navigate to the folder containing the docker-compose file.
- Run the following command:

```
sudo docker-compose -f .\docker-compose-self-hosting.yaml -p penzle-environment up -d
```

### macOS
- Open a terminal window.
- Navigate to the folder containing the docker-compose file.
- Run the following command:

```
docker-compose -f .\docker-compose-self-hosting.yaml -p penzle-environment up -d
```

## How to Access the Services

The Penzle Self-Hosted version contains an all-in-one environment that is ready for development. You can find more details on how to access the specific services and an explanation of what their purposes are.
