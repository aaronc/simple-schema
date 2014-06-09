# fschema

Elegant functional data validation and transformation for Clojure(script).

fschema is intended to provide detailed error messages which can
easily be rendered into human readable (and localizable error messages).

The basic design of the library is to 

## Validator Basics

A validator is any function that takes a value and returns either that
value or an *error* value (any object that responds truthy to the
*error?* function).

The simplest type of validator is a constraint. Constraints can be
created with the *constraint* or the *defconstraint* macro.

Constraints have the following property: for every constraint *c*
other than the *not-nil* constraint, `(= (c nil) nil)`. 

Other types of validators can ve created via composition.

## Mutator Basics

A mutator is any function taking one argument. Mutators may also
return *error* values (see TODO) to signal that an error has occurred.

## Creating Schemas

### defschema

## Composing validators and mutators

### vchain & mchain

### validate-each & mutate-each

### validate-where & mutate-where

### validate-all & mutate-all

## Creating Constraints

### constraint

### defconstraint

## Built-in Constraints

### not-nil

### string?, map?, seq?, number?, boolean?, keyword?, symbol?

### re-matches

### =, <, >, <=, >=

### count=, count<, count>, count<=, count>=

## Errors

### error

### error?

## License

Distributed under the Eclipse Public License, the same as Clojure.
