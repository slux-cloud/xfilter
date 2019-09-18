# xfilter
DSL for mongodb filtering, syntax like of SQL, Based on SAP chevrotain https://github.com/SAP/chevrotain

## Main Concepts

Make an UI interface for MongoDB object queries can be a painful development, beeing simplist you need to create an Tree View Component for mount the object. to solve this problem xfilter is an DSL https://www.martinfowler.com/books/dsl.html, in shapes of SQL filter to aproximate to easy filters mongo collections.

# SYNTAX

## Simple Example

'<property>'<filterOperator><value>
  
in mongo collection with two documents:
{
   foo : 'bar'
}
{
   foo : 'bar2'
}

the expression 'foo'$eq"bar"

will filter only the first document

## properties

the property of object is always quoted 

## values
 
### string 
 is doublequoted. ex: "bar"

### integer
 direct declaration ex: 1
 
### number
  dot split decimal ex: 2.17
  
### boolean 
  true or false

### array
  surrounded by brackets, splitted by commas ex: [2.15, 3.18]
 
## Filter Operators

###  equals $eq 
  
  means SQL =  ex: for 

###  not equals $ne
  means SQL <>

### contains

