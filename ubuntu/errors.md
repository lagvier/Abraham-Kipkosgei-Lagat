1. [ERROR 1698 (28000): Access denied for user 'root'@'localhost'](https://stackoverflow.com/questions/39281594/error-1698-28000-access-denied-for-user-rootlocalhost)
2. Trouble shooting problems
- [x] __E: Could not get lock /var/lib/dpkg/lock - open__
  ```
  sudo rm /var/lib/apt/lists/lock
  sudo rm /var/cache/apt/archives/lock
  sudo rm /var/lib/dpkg/lock
  ```
