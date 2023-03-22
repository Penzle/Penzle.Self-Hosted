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

#### Email (SMTP4Dev)
SMTP4Dev is a dummy SMTP server that allows you to test and view emails without actually sending them. To access the SMTP4Dev web interface, open your web browser and navigate to http://localhost:5010. This interface allows you to view and manage the emails received by the service. The SMTP server listens on port 2525 for incoming email messages, and the IMAP server listens on port 1430 for email retrieval.

#### SQL Server
To access the SQL Server instance, you will need to use a SQL Server client, such as SQL Server Management Studio (SSMS), Azure Data Studio, or any other SQL client that supports SQL Server connections. When connecting, use the following information:

- Server: **localhost,1435** (Note the comma between the hostname and port)
- Authentication: **SQL Server Authentication**
- Login: **sa**
- Password: **Penzle2023**

You should now be able to manage the SQL Server instance, create databases, tables, and run SQL queries.

