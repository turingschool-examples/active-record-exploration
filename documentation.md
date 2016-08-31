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

  * AR Method: `.create!`
  * Description: This will create (meaning, perform both new and save in the database) an object or multiple objects. The difference between between create and create! is that create! will raise a "RecordInvalid" error if the validations for the object fail, whereas create on its own does not do this.
  * Example: If you want to create a new student in the database and it requires first name and last name, you might want to record an error if a field is left blank rather than only not save the object.
  
 `student = Student.create!(last_name = "Smith")`
 the return would be something like:
  `puts invalid.record.errors`

  * Anything else?:  This is very similar to the way save! operates. 
  
