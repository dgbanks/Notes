# Oauth (notes from oauth.com)

* requires synthesis of multiple RFCs (request for comments) and drafts
* does not require token type or grant type
* implementers have to make many of their own decisions

## Definitions

**4 main roles:**
###### 1. resource owner (user)
* the person giving access to some portion of their account
* resources = data, service, etc.
* outside systems need permission to act on their behalf


###### 2. resource server (API)
* the server that contains the information being accessed by the third
party application
* accepts and validates access tokens, grants requests, if allowed


###### 3. authorization server (can be same as API)
* what the user interacts with when an app is requesting access to
their account
* displays the oauth prompt to be approved or denied by user
* needs a URL for the auth request and a URL for apps to use to grant
access tokens


###### 4. client (third party app)
* the app attempting to act on user's behalf (access user's resources)
* needs permission to access user's account


**more definitions**
###### Confidential Clients
* clients which have the ability to maintain the confidentiality of the
`client_secret`
* 


###### Public Clients

###### Access Token

###### Refresh Token

###### Authorization Code
