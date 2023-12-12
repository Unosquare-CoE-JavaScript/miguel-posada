**Book You Don´t Know Javascript jet (YDKJSJ)**

- The path. read every chapter and and read again trying to solve some of the exercises
- large concepts is important for digesting to re-reading, practicing and digesting some more
- be patient with the way the reader learn from this book

_Primitive values_

- stay in mind that Null returns and Object insead of null
- "Coercion" is the action of convert from one value type to another

  _Variables_

- working with 'var' and 'let' has its differences. 'var' is to the global scope. 'let' is block-scope. generate errors if not well declared
- coprisson betwee '==' and '===' operators
- coercion comparisons. important to understand because always is compared with primitive vlues
- Objects and classes: is the way that JS suggest organize code using Class Pattern:
  - Inheritance
- Modules: methods are ecplicity exposed as public and is posible to export only defined functions
  - create modules or variables or methods with 'Export' and 'Import' to use this when is neccesary.
- Iterator: use Map and set, get to work with objects and cache functions
- closure: very usefull to avoid performace issues
- This Keyword: characteristic of function execution. tight to the scope of the function wrraped excepts for arrow functions.
- Prototypes: characteristic of Object and linked to objects. when object is created is linked to another that already exists
  that is called "prototype chain"

  **Hoisting**
  if one variable is using declaration with 'var variable = "greeting"' heyword and inside a function is declared with 'let variable= "greeting"'
  the hoisting will propmt a ReferenceError if in the function scope is used before declaration but outside will work well with 'var'
  identify the _target_ in the algothm and the _source_ reference

  _Leical scope_
  lexical scope” is that it’s controlled entirely by the placement of functions, blocks, and variable declarations, in relation to one another.
  how to process variables.

  1. encountering vars declarations in the 'scope manager'
  2. compiler or engine asks the Scope Manager for delcared variables.
  3. undefined variables shows marks errors
     -The building represents our program’s nested scope collec-
     tion. The first floor of the building represents the currently
     executing scope. The top level of the building is the global
     scope.
     You resolve a target or source variable reference by first
     looking on the current floor, and if you don’t find it, taking
     the elevator to the next floor (i.e., an outer scope), looking
     there, then the next, and so on. Once you get to the top floor
     (the global scope), you either find what you’re looking for, or
     you don’t. But you have to stop regardless-

  - is important to undertand the 'lexical scope' of a variable in a single implementation
