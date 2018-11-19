# Coding rules applicable to Panda (aka CRAP)
The purpose of this document is to provide with set of basic rules according to which the Panda code should be written.
Everyone is welcome to amend, improve, extend and comment it. Especialy if one finds the case under review is not covered by CRAP.

# Rules
## Naming
### Let IDEs do they job
Give your functions, especially inteface ones, a descriptive name. Don't be affraid to use several FULL words if it's needed to make the name descriptive enough. We all do use more or less fancy code editors which are capable of auto-completing the code, so most probably you type full name just once.
On the other hand use only this number of words which is necessary to express the purpose of the function.
The same applies to variables.

### Prefere camels over snakes
We use camel case style of naming.
However, there are several cases where `_` is accaptable:
* in case of class member variables we use `m_` to prefix the actual name - this stand from _member_  

### Sounds similar but makes the difference
Use verbs to clearly specify what the funcion would do, and what kind of job is that.
`setBackgroundColor` is good, `backgroundColor` is bad example for name of function used to set some parameter.
`startAnimation` is good as clearly states action and subject - it's supposed to start (acion) an animatin (subject).
`onAnimationFinished` is much better than `animationFinished` to be a name for event handler.
Some kind of exception would be:
`isOperationAllowed` as good, `operationAllowed` as bad example for name of function returning boolean - `is` works as a verb in here.

Variables, as by the nature are rather state holders, should be named using nouns (and adjectives).
Always refer to first naming rule - the name should be self-explaining. 
`state`, `color`, are bad examples, (except for cases when used as object attributes and only in case object has only one attirbute with such meaning - i.e. `led.color` or 'buzzer.state' ). In 

The same applies to variables.




- indentation
- naming
- comments
- braces and spaces
- new lines
- braking long lines
- 
