# Overview

We have 4 different types of APIs:

* Public
* Protected
* Server
* Activities

## Info about Public API
The Public API is a highly-restricted API that gets access to only publicly available information. However, there is no barrier to entry unlike the Protected and Server API.

The Public API, per domain, has only 100 requests per hour, as we intend this API as a lightweight resource for prototyping and/or accessing basic, public information.

The Public API cannot write any data and does not have access to OAuth or any private information, regardless of whether it is considered private or not.

For example, if you wanted to retrieve a user's public information, you would provide the server with the username (for this example, let's use `katniny`), and we would return publicly available data about that user, which is essentially what you'd see when visiting their profile directly.

However, if a user's profile is set to private, **you will not be able to access their data at all, regardless of whether your account has access to their profile**. We are committed to privacy, and if a user chooses to make their account private, we respect their decision and assume they do not want any of their data, public or private, shared through our API.


## Info about Protected API
The Protected API has access to a lot more that you can do with it, however, you need a TransSocial account and an agreement to our [API Terms of Service](https://transs.social/policies/api-terms).

We, at any time, can revoke your access to your access to the Protected API if you violate our API Terms of Service.

The Protected API, per domain, has 5,000 requests per hour and has access to [Permissions](/protected/permissions).

While, at base level, the Protected API can still only read public information, the real power relies on Permissions. When a user authorizes your [Application](/protected/applications) via [OAuth](/protected/using-oauth), you can do lots of thing such as:

- Accessing certain user info
- Writing certain user info, such as bios
- Creating Notes
- Deleting Notes

!!! note
    All of the above assumes you have the correct permissions.

Our Protected API is good for automated bots but not so good that you could make a third-party client.

## Info about Server API
This is for TransSocial's operations and no one can access this.

## Info about Activities API