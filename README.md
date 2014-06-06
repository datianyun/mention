# Mention.js
在mention.js基础上结合项目实际进行的修改，在@后立即进行请求，同时在选定人员后进行空格处理，以及在@后进行人员信息格式的筛选
<img src="http://i.imgur.com/pCvqL.png">




## 以来Dependencies
* <a href="https://github.com/jquery/jquery" target="_blank">jQuery</a>
* <a href="https://github.com/twitter/bootstrap" target="_blank">Typeahead</a>

##用法


`````javascript
$("#multi-users").mention({
    delimiter: '@',
    users: [{
        username: "ashley"
    }, { 
        username: "roger"
    }, { 
        username: "frecklefart123"
    }]
});
`````

## 用户实例
`````javascript
$("#multi-users").mention({
    sensitive: true,
    users: [{
        username: "sarah"
    }, { 
        username: "bigRat"
    }, { 
        username: "roger"
    }, { 
        username: "Ricky"
    }]
});
`````


`````javascript
$("#multi-users").mention({
    queryBy: ['name', 'username'],
    users: [{
        username: "sarah",
        name: "Sarah Jones",
        image: "http://placekitten.com/25/25"
    }, { 
        username: "bigCat",
        name: "Scott Pfaff",
        image: "http://placekitten.com/25/25"
    }, { 
        username: "coderDude",
        name: "Roger Penn",
        image: "http://placekitten.com/25/25"
    }]
});
`````

## Empty Querying

```javascript
$('#multi-users').mention({
    emptyQuery: true,
    typeaheadOpts: {
        items: 10 // Max number of items you want to show
    },
    users: [...]
});
```


## Defaults
`````javascript
$("#multi-users").mention({
    users: [], // Array of Objects
    delimiter: '@', // Username Delimiter
    sensitive : true,
    queryBy: ['name', 'username'],
    typeaheadOpts: { // Settings for Typeahead
        matcher: _matcher, // Mention.js's custom matcher function, don't change
        updater: _updater, // Mention.js's custom updater function, don't change
        sorter: _sorter, // Mention.js's custom sorter function, don't change
    }
});
 
`````
 
### License


