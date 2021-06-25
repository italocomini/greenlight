# Greenlight

1. Script to create the database  

- `CREATE DATABASE greenlight;`  
- `CREATE ROLE greenlight WITH LOGIN PASSWORD 'pa55word';`     
- `CREATE EXTENSION IF NOT EXISTS citext;`   

2. Command to migrate the database  

- New migrate: `migrate create -seq -ext=sql -dir=migrations add_movies_check_constraints`   
- Windows: `Set-Variable -Name "GREENLIGHT_DB_DSN" -Value "postgres://greenlight:pa55word@localhost:5432/greenlight?sslmode=disable"`   
- Unix/Linux: `export GREENLIGHT_DB_DSN='postgres://greenlight:pa55word@localhost:5432/greenlight?sslmode=disable'`
- Run migration:`migrate -path=migrations -database="$GREENLIGHT_DB_DSN" up`  
