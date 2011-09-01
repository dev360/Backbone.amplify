# Backbone Amplify Storage

Full cross browser fall back (IE5 - w00t!) for backbone.js, courtesy of amplify.store.js.

## Usage

Include Backbone.amplify after having included Backbone.js:
    <script type="text/javascript" src="json2.js"></script>
    <script type="text/javascript" src="backbone.js"></script>
    <script type="text/javascript" src="amplify.store.js"></script>
    <script type="text/javascript" src="backbone.amplify.js"></script>

Create your collections like so:

    window.SomeCollection = Backbone.Collection.extend({
      
      localStorage: new Store("SomeCollection"), // Unique name within your app.
      
      // ... everything else is normal.
      
    });
  
Feel free to use Backbone as you usually would, this is a drop-in replacement.

## Browser support

I tested this in IE7, IE9, Firefox 6, Safari 5, and in Chrome 13. The only snag you need to be 
aware of is to remember to include the json2 dependency, which is required for IE<8. If you
can verify that it works for more browsers, shoot me a mail and let me know so I can update.


## Credits

This code was largely based on https://github.com/jeromegn/Backbone.localStorage, but I needed
it to work for IE6/7.

Anyhow, its refactored to use amplify.store to accomplish the fallback. Naturally, I copied 
the tests as well, thank you [Mark Woodall](https://github.com/llad) for the unit tests, and
big thanks to [Jerome Gravel-Niquet](https://github.com/jeromegn).
