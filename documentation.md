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

  * AR Method: Select  
  * Description: Select allows us to return an active record Relation object with data from one or more specific columns from a table. This is a collection of rows from the table, where each object has the data specified in the Select for the row it represents. Any columns excluded from the Select will not be included in the return value, they will be set to nil; even the id will be nil unless you include it in the Select. It can accept symbols as arguments, an it will return columns with the same name as the symbols. Alternatively, you can pass a string which will be embeded in a SQL Select statement. This is useful for doing calculations or manipulation on each row returned by the select. Select is usually the second method in a chain of Active Record methods, after the table or collection and before methods that transform or limit the result.  
  * Example: Students.select(:name, :email).order(:name); Teachers.select('average(Time.now - hire_date) as seniority');  
  * Anything else?: Select only populates the data you ask for. A collection built from a select method will not include any of the columns not listed.  

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

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

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
  
