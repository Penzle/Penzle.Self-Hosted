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

#### Azure Storage (Azurite)
Azurite is an Azure Storage emulator, providing local Blob, Queue, and Table storage services. To interact with the Azure Storage emulator, you can use any compatible tool, library, or SDK that supports Azure Storage, such as Azure Storage Explorer, Azure CLI, or the Azure SDKs for various programming languages.

The connection string for the local Azurite instance is:
```
DefaultEndpointsProtocol=http;AccountName=devstoreaccount1;AccountKey=Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==;BlobEndpoint=http://localhost:10000/devstoreaccount1;QueueEndpoint=http://localhost:10001/devstoreaccount1;TableEndpoint=http://localhost:10002/devstoreaccount1
```
Use this connection string to access the local Azure Storage emulator using your preferred tool or library such as [Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer)

#### Seq
Seq is a log management and analysis platform. You can access the Seq web interface by opening your web browser and navigating to http://localhost:88. The interface allows you to view, search, and analyze the log events generated by the Penzle project.

#### Web (Penzle Web Application)
The Penzle Web Application can be accessed by opening your web browser and navigating to http://localhost:80. This is the user interface for the Penzle project, where you can interact with the application and its features.

#### Penzle API

The Penzle API is a RESTful API that provides programmatic access to the Penzle project's functionality. You can access the API using any HTTP client, such as a web browser, curl, Postman, or an SDK in your preferred programming language such as C# or JavaScript. The base URL for the API is http://localhost:8012. To explore the available API endpoints, you can refer to the [API documentation](https://www.learn.penzle.com/cms/docs/reference).

## Note
Please note that this setup is intended for local development purposes only. Adjust the configurations and security settings accordingly when deploying to a production environment.

## Recommendation
When it comes to choosing between self-hosted and SaaS solutions, we strongly recommend our SaaS platform. With Penzle SaaS, you'll enjoy a range of powerful features that simply aren't available with self-hosted solutions.

For starters, our SaaS solution offers top-notch support to ensure you always have access to the resources you need. Plus, our platform is always up-to-date with the latest features and enhancements, so you can stay ahead of the competition.

With Penzle SaaS, you can also take advantage of a range of time-saving features like automated backups and updates, seamless integration with other tools, and much more.

So if you're ready to take your business to the next level, it's time to switch to Penzle SaaS. Visit our site https://www.penzle.com/pricing now to compare our features and see for yourself why our solution is the clear choice for modern businesses.



