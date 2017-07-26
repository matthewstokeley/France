### frames 

an scss framework

1. `npm install && grunt build`

2. configure the config file ./config

<i>note:</i> frames in ./frames use config variables to create extendable parent classes, mixins and placeholders. frames are organized by concern - accents, layout and type.  tag-level frames for links and buttons are also provided. 

3. extend frames to create blocks etc in ./app 

##### example

```
.block__entity--small {
	// extend an app parent class
	@extend .block__entity;
	// override a property while clustering the compiled css around a property
	@extend .font-size__small;
}
```