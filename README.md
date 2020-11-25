# recipe-app-api
Recipe app api source for Build A Backend REST API with Python &amp; Django Adv, Udemy course


## Deployment

To deploy to a local environment:

- Clone this repo to your local machine
- Create an admin user with `docker-compose run --rm app sh -c "python manage.py createsuperuser"`
- Run `docker-compose up`
- Go to `http://localhost:8000/api/user/create/` and create a user
- Get your auth token from `http://localhost:8000/api/user/token/` using the details from the user created in the previous step
- Any api requests that require authentication should have this token passed in the header (See `ModHeader` section for instructions)
- To get started, go to `http://localhost:8000/api/recipe/`
- To run the test suite, use `docker-compose run -rm app sh -c "python manage.py test && flake8"`



### ModHeader
This [Chrome extension](https://chrome.google.com/webstore/detail/modheader/idgpnmonknjnojddfkpgkljpfnnfcklj) allows you to modify your request headers.

For the purpose of using this API, install the extension, click the `+` icon, and select `request header`. For `name` select `Authorization` and value should be `Token <your auth token string>`

When you're done playing, don't forget to remove these headers, or you will spend the next few hours wondering why you can't log in to any other sites, like my er... friend did :confused:
