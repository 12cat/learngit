<ul>
    <li><a href="#1">子级窗口调用父级窗口window属性</a></li>
</ul>

<h3 id="1">子级窗口调用父级窗口window属性</h3>
> 父级窗口

``` js
    window.child_data = {
                            'name': '12cat',
                            'age': 18
                        };
    window.open('/child.html', '', 'height=740, width=410');
```
> 子级窗口

``` javaScript
    var data = window.opener.child_data;
```
