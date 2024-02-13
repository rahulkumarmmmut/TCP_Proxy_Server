## TCP Proxy Server

This TCP proxy server is an intermediary tool designed to forward data between a client and a remote server, offering opportunities for monitoring, debugging, and modifying the traffic flow.


## Functionalities

**Data Forwarding**: Relays TCP data bidirectionally between client and server.

**Hex Dump**: Provides a hexadecimal and ASCII dump of the transmitted data for analysis.

**Configurable Connection Handling**: Can be configured to either initiate connection to the remote server first or wait for client data.

**Concurrent Handling**: Utilizes ThreadPoolExecutor to handle multiple client connections concurrently.

**Modular Packet Processing**: Includes request_handler and response_handler functions for potential packet modification.

**Timeout Management**: Implements timeouts on network operations to handle non-responsive connections.

**Robust Error Handling**: Catches and logs various socket-related errors during transmission.

**Command-Line Interface**: Supports command-line arguments for easy configuration of local and remote endpoints.

**Resource Cleanup**: Ensures proper closure of all socket connections even in the event of errors.

## Usage
The proxy server is initiated via command-line with parameters for local and remote host details, and whether the server should receive data from the remote host before the client sends data.

**Server**:
```python 
sudo python3 proxy.py 127.0.0.1 21 ftp.sun.ac.za 21 True  
```
**Client**:
```python
ftp 127.0.0.1 21  
```
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
