# WordPress Docker Setup

This project contains a Docker-based WordPress installation with MySQL database.

## Ports
- **WordPress**: http://localhost:83
- **MySQL**: localhost:3309

## Quick Start

1. Start the containers:
```bash
docker-compose up -d
```

2. Access WordPress at: http://localhost:83

3. Follow the WordPress installation wizard

## Stop the containers
```bash
docker-compose down
```

## Stop and remove all data
```bash
docker-compose down -v
```

## Database Credentials
- **Database Name**: wordpress
- **Username**: wordpress
- **Password**: wordpress_password
- **Database Host**: db:3306 (internal) or localhost:3309 (external)
- **Root Password**: wordpress_root_password

## Useful Commands

### View logs
```bash
docker-compose logs -f
```

### Restart containers
```bash
docker-compose restart
```

### Access WordPress container
```bash
docker exec -it wordpress_app bash
```

### Access MySQL container
```bash
docker exec -it wordpress_db bash
```

### Backup database
```bash
docker exec wordpress_db mysqldump -u wordpress -pwordpress_password wordpress > backup.sql
```
