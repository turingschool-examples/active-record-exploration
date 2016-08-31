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

  * AR Method: Count
  * Description: There are three ways to use .count: count all, count by column, and count with options.<br />

	**Count All:**  If you don’t pass any parameters, count will return a count of all the rows in a model.<br />
	**Count by Column:** You can pass a column name to count, and it will count all the rows where that column is present.<br />
	**Count with Group or Select:** You can call count after .group or .select to get more specific counts.<br />
  * Example:<br />
	**Count All:**  <br />
	-	Car.count<br />
	-	# -> The count of all the cars<br /><br />

**Count by Column:** <br />
	-	Car.count(:sunroof)<br />
	-	# -> All the cars that have a value in the sunroof column<br /><br />

**Count with Group or Select:** <br />
	-	Car.group(:make).count<br />
	-	# -> { ’Nissan’ => 80 , ‘Mazda’ => 53 , ’Tesla’ => 1337 }<br />
	-	You can also group multiple columns and then get the count:<br />
	-	Car.group(:model, :color)<br />
	-	# -> { [‘Model S’, ‘red’] => 74, [‘GTR’, ‘silver’] => 55 }<br />
	-	Car.select(:year).count<br />
	-	# -> Count of the different year values in the year column.<br />
  * Anything else?:  Not all valid select methods will work with count.  If it is invalid an error will be thrown

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
  
