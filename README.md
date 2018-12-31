### frames 

an opinionated scss framework.

##### Installation

`npm install && grunt build`


##### A word of caution

`frames` are essentially css components written in scss, making extensive use of `@extend` to implement composition with injection as opposed to 'built-in' but less performative approaches to selecting - cascading and css operators.  Coupled with the `bem` naming convention, this produces highly-specified selectors, and outputs a css file where properties don't repeat. The main flaw, or at least one of them, in the design of this performance-driven approach to element selectors and properties is file size.  Selector performance is already fast - the larger file size (due to repeating selectors) probably outweighs performance and maintenance concerns.  Tests are needed.  In this regard, `frames` is experimental, however, there might be a use case. 

The name is a reference to a common metaphor used to teach theoretical perspectives.

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
	// override a property by inheriting a 
	// typography-specific class.
	// this will output selectors 'clustered' or organized around
	// this property (configured in ./config.scss)
	@extend .font-size__small;
}
```
