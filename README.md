# Neos.Api.Docs

[Swagger UI](https://swagger.io/tools/swagger-ui/) for the Neos API (Neos.Api) on `/api/docs`, where users log in
with their Neos account to try the API.

## Usage

Install the package next to Neos.Api and Neos.OAuth; `/api/docs` then shows the OpenAPI document of `/api`. The docs
are public, calling the API requires logging in with "Authorize": a popup runs the authorization code flow with PKCE of
the public client `neos-api-docs`, which the package declares in `Neos.OAuth.clients`. The token acts as the logged in
user, with the scopes they select.

The package also links the docs from the API's resource metadata
(`/.well-known/oauth-protected-resource/api`). Swagger UI is loaded from jsDelivr, its version is
`Neos.Api.Docs.swaggerUiVersion`.

## License

MIT, see [LICENSE](LICENSE).
