### France 

an opinionated scss framework.

##### Installation

`npm install && grunt build`


##### A word of caution

-vvv

`frames` are essentially css components written in scss, utilizing extended, configured, domain-specific inheritance.

##### Instructions

```
1. configure the config file ./config

frames use config variables to create extendable parent classes, mixins and placeholders. frames are organized by concern - accents, layout and type.  tag-level frames for links and buttons are also provided. 

2. extend frames to create blocks and components in ./app 
```

##### Example

```
.block__entity--modifier {
	// inherit a parent class
	@extend .block__entity;
	// override a property by inheriting a 
	// typography-specific class
	@extend .font-size__small;
}
```
```
@todo separate configuration scss'
@todo sass
```
