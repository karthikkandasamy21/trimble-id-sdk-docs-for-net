## 1.3.2 (2025-07-21)
* Trimble.ID
	- Default leeway time has been added to renew the token 5 mins before expiration  to prevent disruptions and address edge cases where a token might expire during a critical operation. This is addressed for Client Credential Grant type provider

## 1.3.1 (2025-06-17)
* Trimble.ID
	- Removed unsigned assembly jose-jwt in favor of Microsoft.IdentityModel.JsonWebTokens for token validation.

## 1.3.0 (2025-05-15)
* Trimble.ID
	- Cross-process synchronization using lock file to support multi instance simultaneously retrieving the tokens
	- Token storage improvements
	- Improved error handling and retry mechanism in case of transient errors
	- Offline scenerio support to retrieve the info from storage without an active network connections
	- Bug fixes and code smells addressed
	- Strong named assembly

## 1.3.0-beta.20241217 (2024-12-18)
- New Features
    - Token Storage Improvement: Allowed storage of all types of tokens including access_token, id_token, and token expiry information.
    - Offline Support: Added offline support to fetch user information and tokens when there is no internet connection.

## 1.2.1 (2024-07-25)

* Trimble.ID
	- Reference dependency hierarchy issue fix

## 1.2.0 (2024-06-25)

* Trimble.ID
	- Silent Auth support using `prompt=none` that allows applications to indicate whether to display the login UI
	- A new method `RetrieveTokenAsync` introduced to know the token expiry with the access token
	- TokenRefresh event handler is added to notify the token refresh events
	- Some bug fixes and improvements


## 1.1.2 (2024-04-25)

* Trimble.ID
	- Improvement in error handling and some refactoring for token provider classes

## 1.1.1 (2024-02-28)

* Trimble.ID
	- Addressed a backward compatibility issue
	- Improved analytics tracking

## 1.1.0 (2024-01-19)

* Trimble.ID
	- Device Authorization Grant token provider support for input-constrained devices
   	- Some improvements

## 1.0.1 (2023-12-14)

* Trimble.ID
	- Fixed the ValidatedClaimsetProvider incorrectly adds ClockSkew to Now instead of Token Expiry
	- ValidatedClaimsetProvider Return Dictionary instead of JObject

# 1.0.0

An initial stable version of Trimble.ID SDK

- It is a base library for OAuth2.0 related protocol operations. It provides:
    - Discovery of endpoints
    - Supported Grant Types Token Providers
    - Token Validation
    - HTTP Client Handler to access a given API with the access token
    - Token Persistence
