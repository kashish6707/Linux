### The system admin team at xFusionCorp Industries has streamlined access management by implementing group-based access control. Here's what you need to do:

- Create a group named nautilus_developers across all App servers within the Stratos Datacenter.
- Add the user kano into the nautilus_developers group on all App servers. If the user doesn't exist, create it as well.
```
sudo adduser kano
```
```
sudo groupadd nautilus_developers
```
```
sudo usermod -aG nautilus_developers kano
```
