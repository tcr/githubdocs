# markdocs

Generate API documentation in Markdown for your Github repo or *fun*.

```
npm install git+https://github.com/tcr/markdocs
```

Convert a text representation:

```
$ markdocs convert API.txt
converting: API.txt
conversion done: API.md
```

Even insert into an existing Markdown file inbetween &lt;!--markdocs--&gt; ... &lt!--/markdocs--&gt; tags:

```
$ markdocs insert docs/API.txt
insert: docs/API.txt
into: README.md
insertion done: README.md
```


# Examples

Free form pairs of lines (header:description or signature:description) are converted to syntactically messy and visually beautiful Markdown docs.


## Script Example

```
# Pins
Digital and analog pins can be controlled by an object-oriented API.

array<number> hardware.digitalReadPins = []
An array of which pins are digital inputs.

new hardware.Pin (pin, dir or initialOutput, edge)
Create and return `pin` object.
```

Output:

<hr>

### Pins
Digital and analog pins can be controlled by an object-oriented API.

&#x20;<a href="#api-array-number-hardware-digitalReadPins-" name="api-array-number-hardware-digitalReadPins-">#</a> <i>array&lt;number&gt;</i>&nbsp; hardware.<b>digitalReadPins</b> = []  
An array of which pins are digital inputs.

&#x20;<a href="#api-new-hardware-Pin-pin-dir-or-initialOutput-edge-" name="api-new-hardware-Pin-pin-dir-or-initialOutput-edge-">#</a> new hardware.<b>Pin</b> ( `pin`, `dir` or `initialOutput`, `edge` )  
Create and return `pin` object.

<hr>

Markdown:

```
### Pins
Digital and analog pins can be controlled by an object-oriented API.

&#x20;<a href="#api-array-number-hardware-digitalReadPins-" name="api-array-number-hardware-digitalReadPins-">#</a> <i>array&lt;number&gt;</i>&nbsp; hardware.<b>digitalReadPins</b> = []  
An array of which pins are digital inputs.

&#x20;<a href="#api-new-hardware-Pin-pin-dir-or-initialOutput-edge-" name="api-new-hardware-Pin-pin-dir-or-initialOutput-edge-">#</a> new hardware.<b>Pin</b> ( `pin`, `dir` or `initialOutput`, `edge` )  
Create and return `pin` object.
```


# HTTP Example

    # Tweeting

    Retrieve, post, and search tweets.

    GET /:username/tweets
    Get all of a user's tweets, ever! Returns: 

    ```js
    {
      "tweets": [
        {
          "status": "Everything happens so much",
          "datetime": "2013-09-03T00:00:00",
          "username": "horse_ebooks" 
        }
        ...
      ]
    }
    ```

Output:

<hr>

### Tweeting
Retrieve, post, and search tweets.

&#x20;<a href="#api-GET-username-tweets" name="api-GET-username-tweets">#</a> <b>GET</b> /`:username`/tweets  
Get all of a user's tweets, ever! Returns: 

```js
{
  "tweets": [
    {
      "status": "Everything happens so much",
      "datetime": "2013-09-03T00:00:00",
      "username": "horse_ebooks" 
    }
    ...
  ]
}
```


<hr>

Markdown:

    ### Tweeting
    Retrieve, post, and search tweets.

    &#x20;<a href="#api-GET-username-tweets" name="api-GET-username-tweets">#</a> <b>GET</b> /`:username`/tweets  
    Get all of a user's tweets, ever! Returns: 

    ```js
    {
      "tweets": [
        {
          "status": "Everything happens so much",
          "datetime": "2013-09-03T00:00:00",
          "username": "horse_ebooks" 
        }
        ...
      ]
    }
    ```