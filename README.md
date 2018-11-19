# Coding rules applicable to Panda (aka CRAP)
The purpose of this document is to provide with set of basic rules according to which the Panda code should be written.
Everyone is welcome to amend, improve, extend and comment it. Especialy if one finds the case under review is not covered by CRAP.

# Rules
## Naming
### Let IDEs do they job
Give your functions, especially inteface ones, a descriptive name. Don't be affraid to use several FULL words if it's needed to make the name descriptive enough. We all do use more or less fancy code editors which are capable of auto-completing the code, so most probably you type full name just once.
On the other hand use only this number of words which is necessary to express the purpose of the function.
The same applies to variables.

### Class names
Class names start with capital letter. If the name contains more than one word - follow the next rule.

### Prefere camels over snakes
We use camel case style of naming.
However, there are several cases where `_` is accaptable:
* in case of class member variables we use `m_` to prefix the actual name - this stands from _member_ and is helpful to distinguish between function parameters and members inside the code, i.e:
    ```
    LED::LED(bool isOn, Color color): m_isOn(isOn){m_color = color};
    ```
    ```
    static uint8_t m_targetPwmDuty = 0u; //applies to C code too - static variables of the module are substitute of private members.
    ```
* in case of C code we use underscore to separate 'class' from its 'method', i.e.:
    ```
    void LedDriver_setBrightness(uint8_t targetBrightness)
    {
        m_targetPwmDuty = targetBrightness <= 100u ? targetBrightness : 100u;
    }
    ```
    This improves code readability - you clearly see which module implements the method. And, when you writhe the code, you type the module name and let IDE to help you with the list of methods - you don't need to remember all of them.
* Global C preprocessor macros - as they use all capital letters (to indicate you're having affair with such), we need `_` to separate words, i.e:
    `UNUSED_VARIABLE(x)` or `COUNT_OF(x)`


### Sounds similar but makes the difference - the names
Use verbs to clearly specify what the funcion would do, and what kind of job is that.

`setBackgroundColor` is good, `backgroundColor` is bad example for name of function used to set some parameter.

`startAnimation` is good as clearly states action and subject - it's supposed to start (acion) an animatin (subject).

`onAnimationFinished` is much better than `animationFinished` to be a name for event handler.

Some kind of exception would be:
`isOperationAllowed` as good, `operationAllowed` as bad example for name of function returning boolean - `is` works as a verb in here.

Variables, as by the nature are rather state holders, should be named using nouns (and adjectives).
Always refer to first naming rule - the name should be self-explaining. 
`state`, `color`, are bad examples, (except for cases when used as object attributes and only in case object has only one attirbute with such meaning - i.e. `led.color` or 'buzzer.state' ). In 

Probably you noted the pattern - both function names and variables names (the actual name) start with small letter.

## To be defined
- indentation
- naming
- comments
- braces and spaces
- new lines
- braking long lines
- 
