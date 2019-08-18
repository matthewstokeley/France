### frames 

an opinionated scss framework.

##### Installation

`npm install && grunt build`


##### A word of caution

-vvv

`frames` are essentially css components written in scss, utilizing extended, configured, domain-specific, injected/inherited  parents (with extensive use of the `extend` method) as opposed to built-in but less performative approaches to selecting - cascading and css operators.  Together with the `bem` methodology, this produces highly-specific selectors, and outputs a css file where properties don't repeat - rather than new instances of the properties, inheritance takes the form of selector groups. The main flaw, or at least one of them, in the design of this performance-driven approach to element selectors and properties is file size.  Selector performance is already fast - the larger file size (due to repeating selectors) probably outweighs performance and maintenance concerns.  Tests are needed.  In this regard, `frames` is experimental, however, there might be a use case - one of which is extremely rapid, modular and extensible component-centric css development.

The name is a reference to a common metaphor used to teach theoretical perspectives.

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
@todo separate configuration scss'
@todo sass
