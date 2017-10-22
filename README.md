# msh
Centralize all informations about System Management Times

**Other attempts:**

[Version 0.0 - C# ](https://github.com/fbrump/mhs)

[Version 1.0 - Python/Django](https://github.com/fbrump/msh-python)


## Version 2

Propose:
Create one system with multiple services for management all times of the employers on company, or wherever. Using three languages I'm going to practice my knologe on python with Django/Flask, dotnet core and javascript with angular/react.

### Projects Backend
- ESB - Python/Dotnet Core (?)
- [Domain - PointSheet - Dotnet core](https://github.com/fbrump/msh-domain-point-sheet)
- [Domain - Catalog - Django Rest](https://github.com/fbrump/msh-domain-catalog)
- [Domain - Enterprise](https://github.com/fbrump/msh-domain-enterprise)
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

## Domains Objects:

### [Point-sheet](https://github.com/fbrump/msh-domain-point-sheet) [^](https://github.com/fbrump/msh/blob/master/README.md#projects-backend)

* Release
* Point sheet

### [Enterprise](https://github.com/fbrump/msh-domain-enterprise) [^](https://github.com/fbrump/msh/blob/master/README.md#projects-backend)

* Employer
* Employer Contact Mail
* Employer Contact Phone
* Manager
* Manager Contact Mail
* Position
* Company

### [Catalog](https://github.com/fbrump/msh-domain-catalog) [^](https://github.com/fbrump/msh/blob/master/README.md#projects-backend)

* Day of week
* Type Contact Mail
* Type Contact Phone

### ESB [^](https://github.com/fbrump/msh/blob/master/README.md#projects-backend)

* List of employers
* List of companies
* List of positions
* List of point sheets
* List of releases of point sheets
* Save new release
* Save new point sheets
* Update a release
* Update a point sheets
* Delete a release
* Activate/Deactivate employers
* Activate/Deactivate company
* Activate/Deactivate type contact mail
* Activate/Deactivate type contact phone
* Reports (some, need defined)

### UI [^](https://github.com/fbrump/msh/blob/master/README.md#projects-frontend)

* Login employer/manager
* Employer
    * List your point sheet
    * List realises for each point sheet
    * Create your point sheet
    * Update your point sheet
    * Create realieses
    * Update realises
    * Delete realises
* Manager <- Employer:
    * List all point sheets for your company
    * List all employers for your company
    * Delete releases for employers
    * Activate and Deactivate employers
* Company (newer)
