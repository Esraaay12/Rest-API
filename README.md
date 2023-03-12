# Rest-API
rest API usage to response with standard HTTP Error codes :)
We've already came pretty far, but we're not finished yet. Our API has the ability now to handle basic CRUD operations with data storage. That's great, but not really ideal.
In a perfect world everything works smoothly without any errors. But as you might know, in the real world a lot of errors can happen – either from a human or a technical perspective.

You might probably know that weird feeling when things are working right from the beginning without any errors. This is great and enjoyable, but as developers we're more used to things that are not working properly. 😁

The same goes for our API. We should handle certain cases that might go wrong or throw an error. This will also harden our API.

When something goes wrong (either from the request or inside our API) we send HTTP Error codes back. I've seen and used API's that were returning all the time a 400 error code when a request was buggy without any specific message about WHY this error occurred or what the mistake was. So debugging became a pain.

That's the reason why it's always a good practice to return proper HTTP error codes for different cases. This helps the consumer or the engineer who built the API to identify the problem more easily.

To improve the experience we also can send a quick error message along with the error response. But as I've written in the introduction this isn't always very wise and should be considered by the engineer themself.

For example, returning something like "The username is already signed up" should be well thought out because you're providing information about your users that you should really hide.

In our Crossfit API we will take a look at the creation endpoint and see what errors might arise and how we can handle them. At the end of this tip you'll find again the complete implementation for the other endpoints.

Let's start looking at our createNewWorkout method inside our workout controller:
Source :https://www.freecodecamp.org/news/rest-api-design-best-practices-build-a-rest-api/
