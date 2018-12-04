### frames 

an opinionated scss framework.

##### Installation

`npm install && grunt build`


##### A word of caution

`frames` are essentially css components using scss, making extensive use of `@extend` to implement inheritance within the property field, as opposed to cascading or using css operators.  In this regard, `frames` is experimental but there might be a use case.  

##### Instructions

```
1. configure the config file ./config

<i>note:</i> frames in ./frames use config variables to create extendable parent classes, mixins and placeholders. frames are organized by concern - accents, layout and type.  tag-level frames for links and buttons are also provided. 

2. extend frames to create blocks etc in ./app 
```

##### Example

```
.block__entity--small {
	// extend an app parent class
	@extend .block__entity;
	// override a property while clustering the compiled css around a property
	@extend .font-size__small;
}
```
