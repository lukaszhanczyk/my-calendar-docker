# My Calendar Project

## Collaborators

- [lukaszhanczyk](https://github.com/lukaszhanczyk)
- [hubertmadrzejewski](https://github.com/hubertmadrzejewski)
- [NatOrl](https://github.com/NatOrl)

## Technology

- PHP 8.2
- Node 18.15.0
- Postgres 14.1

## Instalation

1. Create folder `my-calendar` on your computer and clone the repositories given below into it
   </br>[my-calendar-react](https://github.com/lukaszhanczyk/my-calendar-react)
   </br>[my-calendar-symfony](https://github.com/lukaszhanczyk/my-calendar-symfony)
   </br>[my-calendar-docker](https://github.com/lukaszhanczyk/my-calendar-docker)</br>
   </br>
2. The directory tree should look like this

   ```bash
   ── my-calendar
      ├── my-calendar-react
      ├── my-calendar-symfony
      └── my-calendar-docker
   ```

3. Open `my-calendar-docker` directory and in terminal use command

   ```bash
   docker-compose up --build
   ```

4. After the containers start correctly, open new terminal and enter php-container bash

   ```bash
   docker exec -it php-container bash
   ```


** In point 4 and 5 you may need administrator privileges (in Linux, use commands with the `sudo` prefix)

   ```bash
    sudo docker-compose up --build
    sudo docker exec -it php-container bash
   ```
** If backend container have different name, please change `php-container` to this name in command from point 5

5. In bash generate key, push migrations, seed and downland articles using custom command

   ```bash
   composer install
   php bin/console doctrine:migrations:migrate
   ```
   
6. Open new terminal and enter frontend sh
   ```bash
   docker exec -it frontend sh
   ```
7. Install all dependencies and start application
   ```bash
   npm install
   npm run dev
   ```
The application is running on port 3000

[ http://localhost:3000/]( http://localhost:3000/)