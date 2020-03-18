# flat-html
This repository is an unfinished project to render HTML from a flatter representation of HTML that looks like this:

```
{
    "data": [
	"-div 'My post'",
	"-div.incoming_msg_img img(src=https://ptetutorials.com/images/user-profile.png,alt=sam)",
	"-div.received_msg div.received_withd_msg p 'My post'",
	"div.received_msg div.received_withd_msg span.time_date 'time'",
	"div.received_msg div.blah 'Blah'"
    ]
}
```

Should generate HTML like this:

```
<div>
    <div>My post</div>
    <div class="incoming_msg_img"><img class="com/images/user-profile" src="https://ptetutorials.com/images/user-profile.png" alt="sam"></div>
    <div class="received_msg">
        <div class="received_withd_msg">
            <p>My post</p><span class="time_date">time</span></div>
        <div class="blah">Blah</div>
    </div>
</div>
```

# Usage

Open `flat-html.html` in your browser and give it a whirl. There's an editor at the top of the screen so you can see what your flat HTML is generating below.
