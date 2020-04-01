![GitHub last commit (branch)](https://img.shields.io/github/last-commit/shipyardsuite/gateway/develop?color=3cafe2&style=flat-square)
![GitHub issues](https://img.shields.io/github/issues/shipyardsuite/gateway?color=3cafe2&style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2020?color=3cafe2&style=flat-square)
![GitHub](https://img.shields.io/github/license/shipyardsuite/gateway?color=3cafe2&style=flat-square)

# gateway

Gateway Service for application routing
 
## Services

| title      | gateway     | port-int | port-ext | image                    | url                                                     | api-endpoints        | description                                 |
| ---------- | ----------- | -------- | -------- | ------------------------ | ------------------------------------------------------- | -------------------- | ------------------------------------------- |
| redis      | **false**   | `6379`   |          | redis:5                  |                                                         |                      | Database for service-discovery and logging. |
| mongodb    | **false**   | `27017`  |          | mongo:3                  |                                                         |                      | Database for user and project data storage. |
| gateway    | **false**   | `9876`   | `8080`   | shipyardsuite/gateway    |                                                         | `/service-endpoints` | Gateway Service for application routing.    |
| connection | **false**   | `3069`   | `3069`   | shipyardsuite/connection |                                                         | `/connection/api`    | Websocket service for external connection.  |
| homepage   | **true**    | `3001`   | `8080`   | shipyardsuite/homnpage   | `/`                                                     | `/homepage/api`      | Main homepage of application.               |
| auth       | **true**    | `3002`   | `8080`   | shipyardsuite/auth       | `/auth/login`, `/auth/register`                         | `/auth/api`          | Authentification service.                   |
|            |             | `3003`   |          |                          |                                                         |                      | **Reserved**                                |
| dashboard  | **true**    | `3004`   | `8080`   | shipyardsuite/dashboard  | `/dashboard`, `/dashboard/user/`, `/dashboard/project/` | `/dashboard/api`     | User Dashboard service.                     |
| notfound   | **true**    | `3005`   | `8080`   | shipyardsuite/notfound   | `/notfound`                                             | `/notfound/api`      | NotFound page management service.           |
| player     | **true**    | `3006`   | `8080`   | shipyardsuite/player     |                                                         | `/player/api`        | Player managemnt service.                   |
| project    | **true**    | `3007`   | `8080`   | shipyardsuite/project    |                                                         | `/project/api`       | Project managemnt service.                  |
| status     | **true**    | `3008`   | `8080`   | shipyardsuite/status     | `/status`                                               | `/status/api`        | Status overview of all services.            |
| user       | **true**    | `3009`   | `8080`   | shipyardsuite/user       |                                                         | `/user/api`          | User management service.                    |

## License

This project is released under the [Apache version 2](LICENSE) license.