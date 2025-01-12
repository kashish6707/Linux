### As part of the temporary assignment to the Nautilus project, a developer named siva requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do:
- Create a user named siva on App Server 1 in Stratos Datacenter. Set the expiry date to 2024-02-17, ensuring the user is created in lowercase as per standard protocol.
  ```
  sudo useradd -e 2024-02-17 siva
  ```
