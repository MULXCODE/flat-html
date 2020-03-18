# flat-html
This repository is an unfinished project to render HTML from a flatter representation of HTML that looks like this:

```
{ "data": [
    "div 'My post'",
    "div.incoming_msg_img img(src=https://ptetutorials.com/images/user-profile.png)",
    "div.received_msg div.received_withd_msg p 'My Post'",
    "div.received_msg div.received_withd_msg span.time_date 'time'",
    "div.received_msg div.blah 'Blah'"
]}
```

Should generate HTML like this:

```
<div>My Post</div>
<div class="incoming_msg_img">
    <img src="https://ptetutorials.com/images/user-profile.png">
</div>

<div class="received_msg">
        <div class="received_withd_msg">
            <p>My Post</p>
            <span class="time_date">time</span>
        </div>
    <div class="blah">
    Blah
    </div>
</div>
```
