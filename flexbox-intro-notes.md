# Intro:
- flexbox arranges items into rows and columbs and items flex based on rules defined
- a flex container is any element that has "display: flex"
    - a flex item is any element directly inside a flex container
- elements can be both flex containers and flex items

##  Growing and Shrinking

- flex declaration is shorthand for 3 properties that you can set on a flex item.   
    - e.g. "flex: 1" equates to: flex-grow: 1, flex-shrink: 1, flex-basis: 0. So "flex: 1" means "flex: 1 1 0"

### flex-grow:
- expects a single number and it the growth factpr
- a flex of 2 to a particular dic in a container will make it grow 2x the size of the others

### Flex-shrink:
- sets the 'shrink factor' of a flex item
- only applies if the size of all flex items is larger than the parent container. e.g. 3 divs in a container have width: 100px, but the parent container is 250 px, then the divs would shrink to fit.
- a default shrink value of 1 means items will shrink evenly.
- you can specify 0 if you dont want items to shrink
- flex items dont necessarily respect given valuyes for width. i.e if parent is big enough, items will grow.. or if parent is too small, items will shrink.

### flex-basis:
- sets the initial size of a flex item, so any flex growing or flex shrinking starts from this baseline size
- using "auto" as flex-basis tells the item to check for a width declaration
**Important Note - flex-basis default value is auto, but when you specify flex: 1, it interprets it as flex: 1 1 0

### flex auto
- with "flex-auto: 1" - it means:
    - f@lex-grow: 1, flex-shrink: 1, flex-basis: auto"

### Commonly used flexbox effects:
1) initial: flex item doesnt grow but can shrink - expands to flex: 0 1 auto
2) auto: flex items can grow and shrink - expands to flex: 1 1 auto
3) none: flex items neither grow nor shrink - expands to 0 0 auto
4) flex: ```<number [1,inf]> ```
