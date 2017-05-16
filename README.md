### Ngrok Clients

### How to use
Depends on your OS, execute this command:

```
# Linux
./ngrok_linux -subdomain <subdomain> -config=ngrok.conf [<ip>:<port>|<port>]

# MacOS
./ngrok_darwin -subdomain <subdomain> -config=ngrok.conf [<ip>:<port>|<port>]

# Windows
./ngrok_windows.exe -subdomain <subdomain> -config=ngrok.conf [<ip>:<port>|<port>]
```

### Example
```
# Create in simple http server
touch index.php
echo "<?php phpinfo();" > index.php
# Open an web server on your machine on the port 8080.
php -S 127.0.0.1:8080 index.php
# Create a tunnel from 127.0.0.1:8080 to our ngrok server at `tunnel.rikkeisoft.design:8080`
./ngrok_darwin -subdomain rikkeisoft -config=ngrok.conf 127.0.0.1:8080
# Open the address which is provided by ngrok server from above command:
open rikkeisoft.tunnel.rikkeisoft.design:8080
# Finally, you will see a webpage which has same content as your local address 127.0.0.1:8080
```

