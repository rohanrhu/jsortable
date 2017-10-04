# jsortable
jquery plugin for making sortable elements

## Examples

### Load

```html
<script type="text/javascript" src="js/jquery-1.11.1.min.js"></script>
<script type="text/javascript" src="js/jquery.event.drag-2.2.js"></script>
<script type="text/javascript" src="js/jquery.jsortable.js"></script>
```

### Vertical

#### HTML

```html
<div class="example1">
    <div class="box1">
        Element 1
    </div>
    <div class="box1">
        Element 2
    </div>
    <div class="box1">
        Element 3
    </div>
    <div class="box1">
        Element 4
    </div>
</div>
```

#### CSS

```css
.box1 {
    background: #505050;
    color: white;
    border-radius: 2px;
    border-bottom: 2px solid rgba(0,0,0,0.2);
    padding: 10px 10px;
    cursor: move;
    font-size: 13px;
    margin-bottom: 5px;
    user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -webkit-user-select: none;
}
```

#### Javascript

```javascript
var $example1 = $('.example1');

$example1.jsortable({
    sortable: '.box1',
    show_target_placeholder: true,
    show_source_placeholder: false
});

$example1.on('jsortable_updated', function (event) {
    console.log($example1.jsortable('getElements'));
});
```

### Horizontal

#### HTML

```html
<div class="example2">
    <div class="box2">
        Element 1
    </div>
    <div class="box2">
        Element 2
    </div>
    <div class="box2">
        Element 3
    </div>
    <div class="box2">
        Element 4
    </div>
    <div class="clear"></div>
</div>
```

#### CSS

```css
.box1 {
    background: #505050;
    color: white;
    border-radius: 2px;
    border-bottom: 2px solid rgba(0,0,0,0.2);
    padding: 10px 10px;
    cursor: move;
    font-size: 13px;
    margin-bottom: 5px;
    user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -webkit-user-select: none;
}
```

#### Javascript

```javascript
$(document).ready(function () {
    $('.example2').jsortable({
        sortable: '.box2',
        show_target_placeholder: true,
        show_source_placeholder: false
    });
});
```

### Events
There is one event in jsortable.

#### jsortable_updated
Fires on update queue

##### Example

```javascript
$example1.on('jsortable_updated', function (event) {
  console.log($example1.jsortable('getElements'));
});
```

### Methods

There is one method in jsortable.

#### getElements()
Get jQuery list sortable elements

##### Return
jQuery array object of elements in order.

##### Example
```javascript
$example1.jsortable('getElements');
```

## License
MIT
