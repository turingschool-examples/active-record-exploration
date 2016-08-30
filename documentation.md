## Active Record Documentation

Ben

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Brendan

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Brian

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Goss

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Chase 

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Calaway
  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Dan

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

David Davydov

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Jasmin

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Jean

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Jesse Spevack

  * AR Method: PLUCK
  * Description: Pluck can be used to query one or more columns from the underlying table of a model. It accepts a list of column names as argument and returns an array of values contained in those columns.
  * Example: Course.pluck(:name) => [American History, Ancient History]; Course.pluck(:name, :instructor) =[[American History, Smith], [Ancient History, Jones]]
  * Anything else?: Pluck directly converts a database result into a Ruby Array, without constructing ActiveRecord objects. This can mean better performance for a large or often-running query. It also means that one can not use ActiveRecord methods on the array or array elements returned by a pluck call. In the above example, Course.pluck(:name) => [American History, Ancient History]; We could not then treat American History as an ActiveRecord object, it is just the data from the Name column of the Course table.

Matt

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Nate

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Raphael

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Ryan

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Sonia

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Susi

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:
  
