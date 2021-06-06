### Migrate

- `migrate create -seq -ext=sql -dir=migrations add_movies_check_constraints`  
- `Set-Variable -Name "GREENLIGHT_DB_DSN" -Value "postgres://greenlight:pa55word@localhost:5432/greenlight?sslmode=disable"`    
- `migrate -path=migrations -database="$GREENLIGHT_DB_DSN" up`  
