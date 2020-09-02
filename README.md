# Nginx Multi Level Reverse Proxy Example

Inside the `proxy` folder:
```bash
docker-compose up
```

Add the following to your `/etc/hosts` file.
```
# Test Nginx Reverse Proxy
127.0.0.1 center.kubernetes.localhost
127.0.0.1 left.kubernetes.localhost
127.0.0.1 right.kubernetes.localhost
```

When you visit your browser:
- http://localhost -> proxy
- http://center.kubernetes.localhost -> kubernetes
- http://left.kubernetes.localhost -> left
- http://right.kubernetes.localhost -> right

This should show that the hostname is passed down in the proxy and used to 
reverse proxy.
