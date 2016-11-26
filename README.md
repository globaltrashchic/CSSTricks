# CSS Tricks

*As time goes by, CSS is becoming more and more powerful and nowadays it allows a lot of possibilities. We've looked at two tricks to help you make your website even better.*

#Our first topic:

##How to centre elements horizontally, including but not limited to CSS properties like display and margin: auto.

####There are a few options, like for example when the width is known :
The first option works when you know the width of the absolutely positioned element. As such it’s not very flexible or responsive.

somelement {
width: 200px;

position: absolute;

left: 50%;

margin-left: -100px
}

####using translate :
The second option works when you don’t know the width of the absolutely positioned element. Excellent for responsiveness but is CSS3…older browsers may have an issue.

somelement {
position: absolute;

left: 50%;

-webkit-transform: translateX(-50%);

transform: translateX(-50%)
}

####This is also an alternative :
The third option works when you don’t know the width of the absolutely positioned element but makes it 100% wide of it’s parent which might not fit the design. If you do know the width, you can use the third option as well and it will center.

somelement {
position: absolute;

left: 0;

right: 0;

margin: auto
}

