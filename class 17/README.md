# Understanding OAuth for Your Application

OAuth is like having a trusted friend vouch for you when you want to access something important. In the digital world, it's a way for your application to access someone else's account or data without needing their password.

## Why is it useful?

Imagine you have a cool app that wants to post updates on your social media. Instead of sharing your super-secret password with the app, you use OAuth. It's like inviting the app in through a back door without giving it the keys.

## How does it work?

1. **You request access**: Your app asks the social media platform for permission to do certain things (like posting updates).
2. **The platform checks with the user**: The platform asks the user, "Hey, is it okay if this app does XYZ on your behalf?" The user decides.
3. **The platform gives a special key**: If the user says yes, the platform gives your app a special key (like a backstage pass) called an "access token."
4. **Your app uses the key**: Your app can now use this key to access the user's account, but it doesn't know the user's password.

## Benefits of OAuth

- **Security**: Users don't need to give away their passwords, which makes it safer.
- **Control**: Users have the power to revoke access if they change their minds.
- **Simplicity**: Apps don't need to know your password, which simplifies things.

# [Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)
This guide shows you how to build a sample app doing various things with "social login" using OAuth 2.0 and Spring Boot.

It starts with a simple, single-provider single-sign on, and works up to a client with a choice of authentication providers: GitHub or Google.

