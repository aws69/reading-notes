# Spring Security Overview

## Authentication
Authentication in Spring Security refers to the process of verifying the identity of a user, ensuring they are who they claim to be. 
This typically involves validating their credentials, such as a username and password, against a stored record in the system. 
Authentication can also involve other methods like token-based authentication, biometrics, or single sign-on.

## Authorization
Authorization, on the other hand, is the process of determining whether an authenticated user has the necessary permissions to perform a specific action or access a particular resource within the application. 
It defines what a user is allowed to do or see based on their role or privileges.

## AuthenticationManager's authenticate() Method
The `authenticate()` method of the `AuthenticationManager` in Spring Security can result in three possible outcomes:

1. **Successful Authentication**: If the provided credentials match those stored in the system, and any other authentication requirements are met (such as account status or expiration), the method returns an authenticated user object.

2. **Authentication Failure**: If the credentials are invalid or any other authentication conditions are not met, the method throws an authentication exception, indicating the failure.

3. **Account Lockout or Disabled**: In some cases, an account might be locked due to too many failed login attempts or disabled by an administrator. This would also result in an authentication exception, preventing access to the system.

# Spring Auth Cheat Sheet

## Step 1: set up a user model and repo

## Step 2: create a controller for that model

## Step 3: UserDetailsServiceImpl implements UserDetailsService

gets a User from the database by username (make sure your repository has the method to make this easy!)

## Step 4: ApplicationUser implements UserDetails

use IntelliJ to implement the methods; make the boolean ones all return true

## Step 5: WebSecurityConfig extends WebSecurityConfigurerAdapter

- has a UserDetailsService
- passwordEncoder bean
- configure AuthManagerBuilder
    - `auth.userDetailsService(userDetailsService).passwordEncoder(passwordEncoder());`
- configure HttpSecurity
    - cors? csrf?
    - matchers for URLs that are allowed
        - ensure that login and signup URLs allowed; also consider homepage etc.
    - formLogin with login page set up
    - logout

```
    @Override
    @Bean
    public AuthenticationManager authenticationManagerBean() throws Exception {
        return super.authenticationManagerBean();
    }
```

## Step 6: registration page
- create it w/ form
- ensure it posts to a route your controller is ready for
- check it's saving in the DB
```
    // maybe autologin?
    Authentication authentication = new UsernamePasswordAuthenticationToken(newUser, null, new ArrayList<>());
    SecurityContextHolder.getContext().setAuthentication(authentication);
```

## Step 7: login page
- create it w/ form
- ensure it posts to the route you specified in web config
- try it out!
- add to a template w/ things about the Principal