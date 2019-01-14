# Authorization

This example shows how to allow only users in certain roles to access a particular action.


## Getting Started

Be sure to update the `appsettings.json` with your Auth0 settings:

```json
{
  "Auth0": {
    "Domain": "Your Auth0 domain",
    "ClientId": "Your Auth0 Client Id",
    "ClientSecret": "Your Auth0 Client Secret",
    "CallbackUrl": "http://localhost:5000/signin-auth0"
  } 
}
```

Then restore the NuGet packages and run the application:

```bash
# Install the dependencies
dotnet restore

# Run
dotnet run
```

You can shut down the web server manually by pressing Ctrl-C.

## Important Snippets

### 1. Specify the Roles who can access a particular action

```csharp
// /Controllers/HomeController.cs

[Authorize(Roles = "admin")]
public IActionResult Admin()
{
    return View();
}
```
Note : Create VS solution and add these files into it.
