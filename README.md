# Backend Operations 
### What happens when you search google.com in the browser and press enter?

# Domain Name System(DNS) REQUEST

When you type google.com in your browser, on your computer or device what generslly hsppens is,a request is sent to the DNS server, which serves as an address book for all domain names.

This then sends back the exact IP address of the server which [google](https://www.google.com) points to.
This address will be like 123.122.130.3 rendering these numbers for humans is not possible to remember, hence the need for servers known as Domain Name System Servers. The domain names are a way for humans to remember easily for Google.com
##
If you had accessed google.com earlier, the browser first checks its cache to see if it has a recent record of that domain name.

If there is a recent copy of the DNS records for that domain, it will use the IP address in the cache to send a request to the server. 

This speeds up the process of resolving the domain name to an IP address because it avoids the need to send a request to the DNS server.

If the browser cache does not find a copy of the recent record of the requested domain, or if the DNS record has changed since the last time it was cached, the browser will send a request to the DNS server to resolve the domain name to an IP address.

This process is called the **DNS lookup process**.

### Let us explore each one of the DNS server processes:
1. If the requested domain name or UR is not present in the browser’s cache, the browser makes a call to the (OS) which is your Operating system, and asks it if it has the address in its cache.

2. If the browser doesn’t find it on the OS cache it then requests the resolver name server cache which is (IPS) Internet Service Provider to check if it has the requested address.

3. If the resolver name server doesn’t find it in its cache, it asks the root name server to give it the location of the top-level domain server (TLD) such as .com or .org, etc.

4. The TLD nameserver responds with the IP address of the authoritative nameserver for the domain.

5. If the IP address of the requested URL is available, the browser then sends a request to the server at the IP address to retrieve the webpage and now finally you see it on your screen.

### TCP/IP
### Now what does it mean?
(TCP/IP)Transmission Control Protocol/Internet Protocol establishes a connection with Google’s server or domain name server you are looking for. 

Once your computer has the IP address for ```google.com``` TCP is a protocol that ensures that the data sent between your computer and Google’s server or domain name you are looking for is delivered correctly, while IP is a protocol that ensures that the data is sent to the correct destination.

This is like communication between the browser and server with the domain name you are looking for, and when the server receives the request it sends back a message acknowledging the request to establish a connection. 

This is just like the **handshake process.**

The server finally sends the requested url```google.com``` with html code to the browser using TCP.
The browser receives the HTML code and uses it to render the webpage on your screen.
Any resources (such as images) that the webpage needs are also requested and received using TCP/IP.

### Firewall
A firewall is a security device that monitors and filters incoming and outgoing network traffic. 
 
It ensures that the data being sent between your computer and Google’s server or servers domain you are searching for is safe and secure from external threats such as hackers and malware.

You can set rules on your firewall to monitor incoming requests. Two main rules are;

  1. You can set a rule to allow or block traffic based on the source and destination of the request. For example, a firewall may be configured to allow only certain IP addresses to access the network.

  2. You can also set a rule to allow or block traffic based on the type of traffic. For example, a firewall may be configured to allow only certain types of traffic (such as HTTP or HTTPS). And to block traffic on certain ports.

### HTTPS/SSL
Once the TCP/IP connection is established, your browser and Google’s server or domains name you would like to access then begin a handshake to establish a secure connection using HTTPS (Hypertext Transfer Protocol Secure), this is a secure version of the HTTP protocol used to transmit data on the internet.

This is used to encrypt the data.

Data is transmitted between your browser and Google’s server or the domain URL server you are trying to access.

SSL (Secure Sockets Layer) is a protocol that provides the encryption and decryption of data.

This ensures that any data exchanged between your computer and Google’s server or domain URL you are looking for is secure and cannot be intercepted by a third party like a hacker.

This gives the clients visiting such websites to have trust in such websites while using them since they know their details are well secured with such websites, so they are able to make transactions safely.

For example on an e-commerce website, you will most probably have to give details of your credit card when purchasing a product you like and you know your credit card information and passwords are safe from hackers.


### Load-Balancer
A load-balancer is a device that distributes incoming network traffic across multiple servers. 

This ensures that the website can handle a large amount of traffic and prevents any one server from being overwhelmed.

This is how a load balancer works in the case of a browser trying to access ```google.com``` the load balancer would receive the incoming request from the browser and then forward it to one of the servers in the Google server network.

This will also work the same way for any domain name you are trying to search for.

### Web Server
It is a software program that is responsible for delivering web content to clients, typically web browsers, in response to their requests.

Once the request is received by one of Google’s servers or the domain URL server you were looking for from the load balancer, it is passed to a web server. 

The web server is responsible for processing the request, generating the HTML, CSS, and JavaScript that make up the webpage, and sending it back to your browser for you to see it.

😆Incase you don't know what a URL is;

It is (a uniform resource locator ) for the domain you are looking for like google.com, etc.
