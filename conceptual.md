### Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?

    Javascript can be run on most internet browsers, while Pyhton usually needs an interpretor to run it. Most commonly, 
    Python is used for server-side scipting and JS is used for client-side scripting Also, JS has UTF-16 encoding and 
    by default Python is encoded as ASCII.

- Given a dictionary like ``{"a": 1, "b": 2}``: , list two ways you
  can try to get a missing key (like "c") *without* your programming
  crashing.

    try:
        dictionary['c']
    except: 
        print('Key not found')

    ---------------------------------

    if dictionary['c']:
        dictionary['c']


- What is a unit test?

    Unit tests are tests that focus on an individual method, just one specific part of the whole.

- What is an integration test?

    Integration testing is when multiple connected methods are tested together, few pieces that work in accordance for the whole.

- What is the role of web application framework, like Flask?

    Flask is a designed to support the development of web applications, services, APIs, and other resources. Flask includes all
    the tools and libraries necessary to easily complete theses tasks efficiently.

- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?

    The query string parameters are generally describing the current object in reference to the for the object itself. This case
    makes most sense to use '/foods/pretzel' then use a query string if differentiating between pretzels: '/foods/pretzel?type=chocolate' or '/foods/pretzel?type=soft'

- How do you collect data from a URL placeholder parameter using Flask?

    Ex. for /foods -->

    @app.route('/foods/<x>')

    def getFood(x)"
        food = x

- How do you collect data from the query string using Flask?

    Ex. for /foods -->

    @app.route('/foods')

    def getFoodType():
        type = request.args.get('type')

- How do you collect data from the body of the request using Flask?

    Ex. for /foods -->

    @app.route('/foods')

    def getBodyData():

        data = request.form.get('type')

- What is a cookie and what kinds of things are they commonly used for?

    A cookie is data associated with the user's computer IP and is accessed when visiting a website. For examples are the "remember username"
    feature, or search history recommendations.

- What is the session object in Flask?

    The session object in Flask is similar to a cookie however, it only lasts so long as the window is open and also is not affected by browser refreshes. 

- What does Flask's `jsonify()` do?

    Flask's `jsonify()` funtion returns a response object with the application/json MIME(Multipurpose Internet Mail Extensions)type, which is a string that 
    identifies what format to use with the file sent. Also it will convert multiple args into arrays or multiple keyword args into a dict.