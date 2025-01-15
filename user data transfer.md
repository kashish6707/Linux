### Due to an accidental data mix-up, user data was unintentionally mingled on Nautilus App Server 2 at the /home/usersdata location by the Nautilus production support team in Stratos DC. To rectify this, specific user data needs to be filtered and relocated. Here are the details:
Locate all files (excluding directories) owned by user mark within the /home/usersdata directory on App Server 2. Copy these files while preserving the directory structure to the /media directory.
- ssh into app server 2
- use find command to locate all files owned by mark in the /home/usersdata directory, excluding directories.
  ```
   find /home/usersdata -type f -user mark
  ```
- Use the find command combined with cp --parents to copy the files while preserving the directory structure.
  ```
   find /home/usersdata -type f -user mark -exec cp --parents {} /media \;
 ```
- /home/usersdata: Directory to search in.

- type f: Locate files (excluding directories).

- user john: Find files owned by the user mark.

- exec cp --parents {} /media \;: For each file found, execute the cp --parents command to copy the file to the /blog directory, preserving the directory structure.
