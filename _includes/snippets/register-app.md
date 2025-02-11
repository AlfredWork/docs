After you signed up for Criipto Verify, you must register an application before you can actually try logging in with any e-ID.

Once you register your application you will also need some of the information for communicating with Criipto Verify. You get these details from the settings of the application in the dashboard.

Specifically you need the following information to configure you application

- _Client ID_ to identify you application to Criipto Verify. In the case below we chose `urn:criipto:samples:no1`
- _Domain_ on which you will be communicating with Criipto Verify. Could be for example `samples.criipto.id`

![Register App](/images/register-app.png)

### Register callback URLs

Before you can start sending authentication requests to Criipto Verify you need to register the URLs on which you want to receive the returned *JSON Web Token*, JWT.

The Callback URL of your application is the URL where Criipto Verify will redirect to after the user has authenticated in order for the OpenID Connect ASP.NET middleware to complete the authentication process.

You will need to add this URL to the list of allowed URLs for your application. The Callback URL for the sample project project is https://localhost:5001/callback and http://localhost:5000/callback, so be sure to add this to the Callback URLs section of your application. Put each URL on a new line.

![Callback URLs]({{include.callback-urls-img}})

If you deploy your application to a different URL you will also need to ensure to add that URL to the Callback URLs. 


