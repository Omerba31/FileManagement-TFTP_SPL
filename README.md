# File Management System with TFTP

## Overview
This project is a **Java-based file management system** with an integrated **Trivial File Transfer Protocol (TFTP) client and server**. It implements network communication protocols for efficient file transfers and multi-threading for handling multiple connections.

## Features
✅ Multi-threaded TFTP server and client  
✅ Supports file uploads and downloads  
✅ Implements networking protocols for file management  
✅ Configurable settings via `config.properties`  
✅ Built with Java and Maven for easy dependency management  

## Project Structure
```
FileManagement-TFTP/
├── client/                     # Client-side implementation
│   ├── src/main/java/          # Java source code for client
│   ├── resources/              # Configuration files
├── server/                     # Server-side implementation
│   ├── src/main/java/          # Java source code for server
│   ├── resources/              # Configuration files
├── README.md                   # Project documentation
├── .gitignore                   # Ignore unnecessary files
└── pom.xml                      # Maven build file
```

## Installation & Build
### Prerequisites
- Java 8+ installed
- Maven installed

### Steps to Build
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/FileManagement-TFTP.git
   cd FileManagement-TFTP
   ```
2. Build the project using Maven:
   ```sh
   mvn clean install
   ```

## Running the Application
### Start the TFTP Server
```sh
cd server
mvn compile exec:java -Dexec.mainClass="bgu.spl.net.impl.tftp.TftpServer" -Dexec.args="7777"
```
- `7777` → The port number the server will listen on.

### Start the TFTP Client
```sh
cd client
mvn compile exec:java -Dexec.mainClass="bgu.spl.net.impl.tftp.TftpClient" -Dexec.args="127.0.0.1 7777"
```
- `127.0.0.1` → The IP address of the server (local machine).
- `7777` → The port the client should connect to.

## Configuration
Modify `config.properties` in `resources/` to adjust file management settings such as:
```
# Server port
port=69

# Maximum connections
maxClients=10
```

## Running Tests
To run unit tests:
```sh
mvn test
```

## Contributing
1. Fork the repository
2. Create a new branch (`git checkout -b feature-name`)
3. Commit changes (`git commit -m "Added feature"`)
4. Push branch (`git push origin feature-name`)
5. Submit a pull request

## License
[MIT License] - Free to use and modify.

## Author
Developed as part of a **Software Programming Laboratory (SPL) Assignment**.

