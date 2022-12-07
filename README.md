# BuberDinner
[Youtube playlist](https://www.youtube.com/playlist?list=PLzYkqgWkHPKBcDIP5gzLfASkQyTdy0t4k)
## Repository pattern

**Microsoft docs**: `Repositories are classes or componets that encapsualte the logic required to acces data sources.`

**Martin Fowler**: `Mediates between the domain and data mapping layers using a collection-like interface for accesing domain objects.` 

## Options pattern

**Microsoft docs**: `The options pattern uses classes to provide strongly typed access to groups of related settings.`

- [BuberDinner.Application/Common/Interfaces/Authentication/JwtSettings.cs](BuberDinner.Application/Common/Interfaces/Authentication/JwtSettings.cs) 
- [BuberDinner.Infrastructure\DependencyInjection.cs](BuberDinner.Infrastructure\DependencyInjection.cs)
- [BuberDinner.Infrastructure\Authentication\JwtTokenGenerator.cs](BuberDinner.Infrastructure\Authentication\JwtTokenGenerator.cs)

## Problem details Response Specifitacion

### Example

```json 

   HTTP/1.1 403 Forbidden
   Content-Type: application/problem+json
   Content-Language: en

   {
    "type": "https://example.com/probs/out-of-credit",
    "title": "You do not have enough credit.",
    "detail": "Your current balance is 30, but that costs 50.",
    "instance": "/account/12345/msgs/abc",
    "balance": 30,
    "accounts": ["/account/12345",
                 "/account/67890"]
   }
```
see : [rfc specification](https://www.rfc-editor.org/rfc/rfc7807):
