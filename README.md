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

##Center Align Elements

To horizontally center a block element (like <div>), use margin: auto;

Setting the width of the element will prevent it from stretching out to the edges of its container.

The element will then take up the specified width, and the remaining space will be split equally between the two margins:

####Example

.center { 

    margin: auto;
    width: 50%;
    border: 3px solid green;
    padding: 10px;
    
}

##Center Align Text

To just center the text inside an element, use text-align: center;

####Example

.center {
    
    text-align: center;
    border: 3px solid green;
    
}

##Center Align Text

To just center the text inside an element, use text-align: center;

####Example

.center {

    text-align: center;
    border: 3px solid green;
    
}

##Center an Image

To center an image, use margin: auto; and make it into a block element:

####Example

img {
    
    display: block;
    margin: auto;
    width: 40%;
    
}

## [Centering Things](https://www.w3.org/Style/Examples/007/center.en.html)

#Our second topic:

##CSS Transitions

*CSS3 transitions allows you to change property values smoothly (from one value to another), over a given duration.*

*An example of this is hovering your mouse over a button and the button enlarges and changes colour.*

####How to Use CSS3 Transitions?

To create a transition effect, you must specify two things:

*the CSS property you want to add an effect to
*the duration of the effect

**Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.**

The following example shows a 100px * 100px red <div> element. The <div> element has also specified a transition effect for the width property, with a duration of 2 seconds:

####Example

div {

    width: 100px;
    height: 100px;
    background: red;
    -webkit-transition: width 2s; /* Safari */
    transition: width 2s;
    
}

######The transition effect will start when the specified CSS property (width) changes value.

######Now, let us specify a new value for the width property when a user mouses over the <div> element:

####Example

div:hover {

    width: 300px;
    
}


####Change Several Property Values

The following example adds a transition effect for both the width and height property, with a duration of 2 seconds for the width and 4 seconds for the height:

####Example

div {
    -webkit-transition: width 2s, height 4s; /* Safari */
    transition: width 2s, height 4s;
}

####Specify the Speed Curve of the Transition

The transition-timing-function property specifies the speed curve of the transition effect.

The transition-timing-function property can have the following values:

ease - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
linear - specifies a transition effect with the same speed from start to end
ease-in - specifies a transition effect with a slow start
ease-out - specifies a transition effect with a slow end
ease-in-out - specifies a transition effect with a slow start and end
cubic-bezier(n,n,n,n) - lets you define your own values in a cubic-bezier function
The following example shows the some of the different speed curves that can be used:

####Delay the Transition Effect

The transition-delay property specifies a delay (in seconds) for the transition effect.

The following example has a 1 second delay before starting:

####Example

div {
    -webkit-transition-delay: 1s; /* Safari */
    transition-delay: 1s;
}

## [How to use CSS transition](http://www.w3schools.com/css/css3_transitions.asp)
