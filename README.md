# ontos-app-routing
Custom app routing for Ontos Polymer-Apps. 
This element will update the app URL depending on the authentication status and may redirect to the login page. 
Therefore you will need to update a boolean that reflects the authentication status (value `true` for authenticated).

## Usage
Use this element in combination with an `<iron-pages>` element as shown below. 

```html
<ontos-app-routing auth-valid="[[someBooleanIfAuthenticated]]" 
                   login-page="theIdOfTheLoginPage"
                   default-page="theIdOfTheLandingPage" 
                   page="{{thisIsTheCurrentPage}}" 
                   use-hash-as-path> 
</ontos-app-routing> 

<iron-pages selected="[[thisIsTheCurrentPage]]" attr-for-selected="id"> 
	<the-login-page id="theIdOfTheLoginPage"></the-login-page> 
	<the-landing-page id="theIdOfTheLandingPage"></the-landing-page> 
	<some-page id="foo"></some-page>
	<some-other-page id="bar"></some-other-page> 
</iron-pages> 
```

The `use-hash-as-path` parameter is used as in the standard polymer `<app-location>` element.