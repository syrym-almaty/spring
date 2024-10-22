# Java Development and QA Environment Setup with Git Tools via Scoop

This guide provides step-by-step instructions for setting up a **Java development environment** using **Scoop**, installing tools for **Quality Assurance (QA)**, and adding **Git-related tools** to manage source control efficiently.

## Prerequisites

- **PowerShell 7** (or higher).
- **Scoop** (if not installed, install it by running the following command in PowerShell):

  ```powershell
  iwr -useb get.scoop.sh | iex
  ```

## Step 1: Add Necessary Scoop Buckets

First, add the required Scoop buckets to access a wide range of development, QA, and Git-related tools. Run the following commands to add them:

```powershell
scoop bucket add main
scoop bucket add extras
scoop bucket add versions
scoop bucket add java
scoop bucket add nirsoft
scoop bucket add nonportable
```

### Explanation of Buckets

- **main**: Core development tools.
- **extras**: Additional useful tools for developers.
- **versions**: Older or beta versions of tools.
- **java**: Tools related to Java development.
- **nirsoft**: Useful system utilities.
- **nonportable**: Applications that are not fully portable.

## Step 2: Install Java Development Tools

Install the essential tools for Java development, such as **OpenJDK**, **Maven**, **Gradle**, and **Spring Boot**.

### Install OpenJDK 17

OpenJDK 17 is needed to run Java applications. Install it using:

```powershell
scoop install openjdk17
```

### Install Maven

Maven is used for building and managing Java projects. Install Maven:

```powershell
scoop install maven
```

### Install Gradle

Gradle is a modern build tool for Java projects. Install Gradle:

```powershell
scoop install gradle
```

### Install Spring Boot CLI

Spring Boot is widely used to simplify Java development. Install Spring Boot CLI:

```powershell
scoop install springboot
```

### Set OpenJDK 17 as the Default Version

To ensure **OpenJDK 17** is the default version, run:

```powershell
scoop reset openjdk17
```

### Verify Installations

Run the following commands to verify that the tools are installed:

```powershell
java -version      # Check OpenJDK version
mvn -version       # Check Maven version
gradle -v          # Check Gradle version
spring --version   # Check Spring Boot CLI version
```

## Step 3: Install QA Tools

Install the necessary tools for testing and quality assurance in your Java projects, such as **Postman**, **Swagger**, and **Curl**.

### Install Postman

Postman is a popular tool for API testing. Install it using:

```powershell
scoop install postman
```

### Install Swagger

Swagger is essential for documenting and testing APIs. Install it using:

```powershell
scoop install go-swagger
```

### Install Curl

Curl is used for command-line HTTP requests and API testing. Install Curl:

```powershell
scoop install curl
```

### Verify QA Tools

Verify the installation of QA tools with the following commands:

```powershell
postman           # Launch Postman
swagger version   # Check Swagger version
curl --version    # Check Curl version
```

## Step 4: Install Git and Git-Related Tools

In addition to the Java and QA tools, you will also need **Git** and **Git-related tools** for version control and efficient Git operations.

### Install Git

Git is a version control system essential for source code management. Install Git:

```powershell
scoop install git
```

### Install GitHub CLI

The GitHub CLI allows you to interact with GitHub directly from the command line. Install it using:

```powershell
scoop install gh
```

### Install Git Tools for Enhanced Operations

Install other useful Git-related tools to streamline your Git workflow:

- **Git-LFS** (for managing large files in Git repositories):

  ```powershell
  scoop install git-lfs
  ```

### Verify Git and GitHub Tools

After installation, verify the versions of Git and related tools with the following commands:

```powershell
git --version          # Check Git version
gh --version           # Check GitHub CLI version
git-lfs --version      # Check Git LFS version
```

## Step 5: Keeping All Tools Updated

To keep your tools updated, run the following command periodically:

```powershell
scoop update *
```

This ensures that all your installed packages are up to date.

---

