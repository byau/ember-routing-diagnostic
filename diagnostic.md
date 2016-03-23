# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    <!-- your response here -->
    the router keeps tracks of the urls or the path of each templates.  Inside each route, you will want to include a model hook, which pass the information into the template.  it helps load the appropriate template and the appropriate model.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    <!-- your response here -->
    ember g route boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    <!-- your response here -->
    {{#link-to 'campus.boston'}} {{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    <!-- your response here -->
    first one should how the product and products are related, and 2nd just simply denote the path or url with the product, while the url is after products, it doesn't have to had any relationship with products.

    in the 1st case, the product template can be loaded onto the {{outlet}} in products template, but not in the 2nd case.

    If you loaded case 1, the products template will be loaded to the application, then product template can be loaded to the outlet section of products template.  case 2 will just load product template to the application by-passing products template.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    <!-- your response here -->
    params.movie_id
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    <!-- your response here -->
    model
    ```
