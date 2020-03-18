# flat-html
This repository renders HTML from a flatter representation of HTML that looks like this:

```
    "data": [
        "-div 'My post'",
        "-div.mesgs div.mesg_history div.incoming_msg_img img(src=https://ptetutorials.com/images/user-profile.png,alt=sam)",
        "div.mesgs div.mesg_history div.received_msg div.received_withd_msg p 'My post'",
        "div.mesgs div.mesg_history div.received_msg div.received_withd_msg span.time_date 'time'",
        "div.mesgs div.mesg_history div.received_msg span.blah 'Mixed '",
        "div.mesgs div.mesg_history div.received_msg span.blah 'elements '",
        "div.mesgs div.mesg_history div.received_msg b 'go down a treat'",
		
		"-div.mesgs div.mesg_history div.incoming_msg_img img(src=https://ptetutorials.com/images/user-profile.png,alt=sam)",
        "div.mesgs div.mesg_history div.received_msg div.received_withd_msg p 'My post'",
        "div.mesgs div.mesg_history div.received_msg div.received_withd_msg span.time_date 'time'",
        "div.mesgs div.mesg_history div.received_msg span.blah 'Mixed '",
        "div.mesgs div.mesg_history div.received_msg span.blah 'elements '",
        "div.mesgs div.mesg_history div.received_msg b 'go down a treat'"
		
    ]
```
It's an alternative to templating and helpful in debugging complicated HTML. You can use cursor tools of your text editor to rename classes in columns mode.

It should generate HTML like this:

```
<div>
    <div>My post</div>
    <div class="mesgs">
        <div class="mesg_history">
            <div class="incoming_msg_img"><img class="com/images/user-profile" src="https://ptetutorials.com/images/user-profile.png" alt="sam"></div>
            <div class="received_msg">
                <div class="received_withd_msg">
                    <p>My post</p><span class="time_date">time</span></div><span class="blah">Mixed </span><span class="blah">elements </span><b>go down a treat</b></div>
        </div>
    </div>
    <div class="mesgs">
        <div class="mesg_history">
            <div class="incoming_msg_img"><img class="com/images/user-profile" src="https://ptetutorials.com/images/user-profile.png" alt="sam"></div>
            <div class="received_msg">
                <div class="received_withd_msg">
                    <p>My post</p><span class="time_date">time</span></div><span class="blah">Mixed </span><span class="blah">elements </span><b>go down a treat</b></div>
        </div>
    </div>
</div>
```

# Usage

Open `flat-html.html` in your browser and give it a whirl. There's an editor at the top of the screen so you can see what your flat HTML is generating below.
