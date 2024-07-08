---

# TCPCommLib: TCP Communication Library in C

This repository contains a C library for implementing TCP communication, including functionalities for sending and receiving data over a TCP connection.

## Features

- **TCP Sender and Receiver**: Modules for sending and receiving data over TCP.
- **Linked List Implementation**: Utility functions for managing data using linked lists.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/WasiimSheb/TCPCommLib.git
    ```
2. Navigate to the project directory:
    ```bash
    cd TCPCommLib
    ```

## Compilation

Compile the source code using the provided `Makefile`:
```bash
make
```

## Usage

### Example

Here is a basic example of how to use the TCP communication library:

#### Sender
```c
#include "TCP_Sender.h"

int main() {
    // Initialize sender
    tcp_sender_init("127.0.0.1", 8080);
    
    // Send data
    char data[] = "Hello, TCP!";
    tcp_send(data, sizeof(data));
    
    // Clean up
    tcp_sender_close();
    return 0;
}
```

#### Receiver
```c
#include "TCP_Receiver.h"

int main() {
    // Initialize receiver
    tcp_receiver_init(8080);
    
    // Receive data
    char buffer[1024];
    tcp_receive(buffer, sizeof(buffer));
    
    // Print received data
    printf("Received: %s\n", buffer);
    
    // Clean up
    tcp_receiver_close();
    return 0;
}
```

## Files and Directories

- **TCP_Sender.c / TCP_Sender.h**: Implementation and header files for the TCP sender module.
- **TCP_Receiver.c / TCP_Receiver.h**: Implementation and header files for the TCP receiver module.
- **List.c / List.h**: Implementation and header files for the linked list utility functions.
- **Makefile**: Makefile for compiling the project.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Contact

For any inquiries, please contact: Wasimshebalny@gmail.com

---
