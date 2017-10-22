# msh
Centralize all informations about System Management Times

**Other attempts:**

Version 0.0 - C# - https://github.com/fbrump/msh

Version 1.0 - Python/Django - https://github.com/fbrump/msh-python


## Version 2

Propose:
Create one system with multiple services for management all times of the employers on company, or wherever. Using three languages I'm going to practice my knologe on python with Django/Flask, dotnet core and javascript with angular/react.

### Projects Backend
- ESB - Python/Dotnet Core (?)
- Domain - PointSheet - Dotnet core.
- Domain - Catalog - Django Rest
- Domain - Enterprise
- Domain - Auth - Python/Dotnet Core (?)
- Unittest: Unit (donet core), unittest/pytests (python)

### Projects Frontend
- Angular (4..) front-end
- NodeJs (host front-end code)

### Databases
- Database Domains: PostgreSql
- Database logs: Mongodb/Redis

### Server/Hosting
- Hosting Nginx (linux server)

## Structure proposed

Create one project for front end, this will call ESB project, that manager what domain do you nee call; one domain just access ESB, but ESB call all domains. If domain 1 need call other domain 2, it will call ESB, ESB will call Domain 2 that return to ESB will retorne Domain 1. Basically! Let's go.

