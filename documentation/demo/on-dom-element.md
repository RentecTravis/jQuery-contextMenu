# Demo: Menu Title

<ul id="the-node">
    <li><span class="context-menu-one label label-default">right click me 1</span></li>
    <li><span class="context-menu-one label label-default">right click me 2</span></li>
    <li>right click me 3</li>
    <li>right click me 4</li>
</ul>

## Example code

<script type="text/javascript" class="showcase">
$(function(){
    $('#the-node').contextMenu({
        selector: 'li', 
        callback: function(key, options) {
            var m = "clicked: " + key + " on " + $(this).text();
            window.console && console.log(m) || alert(m); 
        },
        items: {
            "edit": {name: "Edit", icon: "edit"},
            "cut": {name: "Cut", icon: "cut"},
            "copy": {name: "Copy", icon: "copy"},
            "paste": {name: "Paste", icon: "paste"},
            "delete": {name: "Delete", icon: "delete"},
            "sep1": "---------",
            "quit": {name: "Quit", icon: function($element, key, item){ return 'icon icon-quit'; }}
        }
    });
});
</script>

## Example HTML
<div style="display:none;" class="showcase" data-showcase-import=".context-menu-one"></div>