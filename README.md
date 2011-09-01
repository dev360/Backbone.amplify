# Backbone Amplify storage

Lets you store anything anywhere.

Full cross browser fall back (IE5 - w00t!) for backbone.js, courtesy of amplify.store.js.

## Usage

Include Backbone.amplify after having included Backbone.js:

    <script type="text/javascript" src="backbone.js"></script>
    <script type="text/javascript" src="amplify.store.js"></script>
    <script type="text/javascript" src="backbone.amplify.js"></script>

Create your collections like so:

    window.SomeCollection = Backbone.Collection.extend({
      
      localStorage: new Store("SomeCollection"), // Unique name within your app.
      
      // ... everything else is normal.
      
    });
  
Feel free to use Backbone as you usually would, this is a drop-in replacement.

## Credits

This code was largely based on https://github.com/jeromegn/Backbone.localStorage, but I needed
it to work for IE6/7, plus allow for regular REST backed access whenever a collection did not
have a store attribute.
Anyhow, its refactored to use amplify.store to accomplish the fallback. Naturally, I copied 
the tests as well, thank you [Mark Woodall](https://github.com/llad) for the unit tests, and
big thanks to Jerome Gravel-Niquet.
