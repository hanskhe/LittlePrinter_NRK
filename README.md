# Little Printer Hello World Example (Python)

This is an example publication, written in Python using the [Flask framework](http://flask.pocoo.org/). The same example can also be
seen in:

* [PHP](https://github.com/bergcloud/lp-hello-world-php)
* [Ruby](https://github.com/bergcloud/lp-publication-hello-world)

This example shows how to set up and validate a form for a subscriber to
configure the publication.

Read more about this example [on the developer site](http://remote.bergcloud.com/developers/littleprinter/examples/hello_world). 

## Configuration

By default the application is run with `DEBUG=False`. To change this create a file at `lp-hello-world-python/settings.cfg` containing this:

    DEBUG = True

Then set the `HELLOWORLD_SETTINGS` environment variable to point to this:

    $ export HELLOWORLD_SETTINGS=./settings.cfg

On Windows use this instead:

    >set HELLOWORLD_SETTINGS=.\settings.cfg

Flask can be installed using [pip](https://pypi.python.org/pypi/pip):

	$ pip install -r requirements.txt

## Run it

Run the server with:

	$ python publication.py

You can then visit these URLs:

* `/edition/?lang=english&name=Phil&local_delivery_time=2013-11-11T12:20:30-08:00`
* `/icon.png`
* `/meta.json`
* `/sample/`

In addition, the `/validate_config/` URL should accept a POST request with
a field named `config` containing a string like:

    {"lang":"english","name":"Phil"}
    

----

BERG Cloud Developer documentation: http://remote.bergcloud.com/developers/

