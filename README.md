# Chatbox
this is a Streamlabs Chat box CSS style

---
### HTML
```HTML
<!-- item will be appened to this layout -->
<div id="log" class="sl__chat__layout">
</div>

<!-- chat item -->
<script type="text/template" id="chatlist_item">
  <div data-from="{from}" data-id="{messageId}">
    <span class="meta" style="color: {color}">
      <span class="badges">
      </span>
      <span class="name">{from}</span>
    </span>

    <span class="message">
      {message}
    </span>
  </div>
</script>
```

### CSS
```CSS
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@500;700&display=swap');

* {
    box-sizing: border-box;
}

html, body {
    height: 100%;
    width: 100%
    overflow: hidden;
}

body {
    text-shadow: 0 0 1px #000, 0 0 2px #000;
    font-family: 'Noto sans TC';
    font-weight: 500;
    font-size: 18px;
    line-height: 1.2em;
    color: #FFFFFF;
}

#log>div {
    animation: fadeInRight .3s ease forwards, fadeOut 0.5s ease {message_hide_delay} forwards;
    -webkit-animation: fadeInRight .3s ease forwards, fadeOut 0.5s ease {message_hide_delay} forwards;
}

.colon {
    display: none;
}

#log {
    display: table;
    position: absolute;
    bottom: 0;
    left: 0;
    padding: 0 5px 5px;
    width: 100%;
    table-layout: relative;
}

#log>div {
    display: table-row;
}

#log>div.deleted {
    visibility: hidden;
}

#log .emote {
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    padding: 0.4em 0.2em;
    position: relative;
}

#log .emote img {
    display: inline-block;
    height: 1em;
    opacity: 0;
}

#log .message,#log .meta {
    vertical-align: top;
    display: table-cell;
    padding-bottom: 0.1em;
}

#log .meta {
    width: 25%;
    text-align: left;
    padding-right: 1em;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
}

#log .message {
    word-wrap: break-word;
    width: 100%;
  
  background-color: rgba(75,75,75,0.8);
  box-shadow: 0 0.5em 2rem rgba(38,50,56,0.1);
  border-radius: 5em;
  border-top-left-radius: 0.125em;
  display: block;
  padding: 0.5rem;
	margin-bottom: 0.3rem;
}

.badge {
    display: inline-block;
    margin-right: 0.2em;
    position: relative;
    height: 1em;
    vertical-align: middle;
    top: -0.1em;
}

.name {
    font-family: 'Noto sans TC';
    font-weight: 700;
}
```

### JS

```js
// Please use event listeners to run functions.
document.addEventListener('onLoad', function(obj) {
	// obj will be empty for chat widget
	// this will fire only once when the widget loads
});

document.addEventListener('onEventReceived', function(obj) {
  	// obj will contain information about the event
	
});
```
