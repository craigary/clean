<p align="center"> 
    <img src="https://github.com/salihciftci/clean/blob/master/src/home.png?raw=true" width="500">
</p>

# Clean
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) 

Tag based responsive [Ghost](https://ghost.org/) theme.


## Manual Installation

We need to setup clean manually because listing tag posts is currently not possible in ghost. For more information check it out ErisDS's [answer](https://stackoverflow.com/a/30381801) on stackoverflow.

Here is the sample code about how to get all posts in specific tag;

``` hbs
<a id="Networking"></a>
<h2>Networking</h2>
{{#get "posts" filter="tags:networking"}}
    {{#foreach posts}}
    <h3>
        <a href="{{url}}">{{title}}</a>
        <span class="main-time">
            <time class="post-date" datetime="{{date format='YYYY-MM-DD'}}">{{date format="DD MMM YYYY"}}</time>
        </span>
    </h3>
    {{/foreach}}
{{/get}}
```

We need to edit get function for our tags.
```hbs
{{#get "posts" filter="tags:networking"}}
```

Change the ```tags``` property for listing post in specific tag. In this example currently I'm listing all posts in ```networking``` tag. If you wanna limit the count of post we can use limit property.

``` hbs
{{#get "posts" filter="tags:networking" limit="5"}}
```

We used semicolons because limit is a string. For more information check [ghost docs](https://themes.ghost.org/docs/get).

And thats it.

## Screenshots


![](https://github.com/salihciftci/clean/blob/master/src/home.png?raw=true)
![](https://github.com/salihciftci/clean/blob/master/src/post.png?raw=true)

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/salihciftci/clean/blob/master/LICENSE) file for details
