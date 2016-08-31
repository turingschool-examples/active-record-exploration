## Active Record Documentation

Ben

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Brendan

  * AR Method: `average`
  * Description: Given one column on a table, `average` finds the mean of the values in that column.
  * Example: `Item.average(:price)`
  * Anything else?: Conditions for what values to average can be passed in as an argument, like
   + `Item.average(:price, conditions:["price < 50"])`

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
  * AR Method: having
    * Description: `having` is always used in conjuction with `group`. Think of it as "group where." (Note that `where` cannot be called after `group`, hence the need for a different method).
  * Example: 
    * Find all products for which the price is the same as at least 4 other products. Said another way, group all products by those that have the same prices, then count how many items share the same prices, then return only the collections of products for which that count is 5 or more. So group by price where that count is greater than 4.
    * `Product.group(:price).having("count(price) > 5")`
  * Anything else?:
    * Input: result of a group query (an ActiveRecord object)
    * Output: new ActiveRecord object with a collection of elements matching the group/having combination.

Dan

  * AR Method: Count
  * Description: There are three ways to use .count: count all, count by column, and count with options.<br />

	**Count All:**  If you don’t pass any parameters, count will return a count of all the rows in a model.<br />
	**Count by Column:** You can pass a column name to count, and it will count all the rows where that column is present.<br />
	**Count with Group or Select:** You can call count after .group or .select to get more specific counts.<br />
  * Example:<br />
	**Count All:**  <br />
		Car.count<br />
		# -> The count of all the cars<br />

	**Count by Column:** <br />
		Car.count(:sunroof)<br />
		# -> All the cars that have a value in the sunroof column<br />

	**Count with Group or Select:** <br />
		Car.group(:make).count<br />
		# -> { ’Nissan’ => 80 , ‘Mazda’ => 53 , ’Tesla’ => 1337 }<br />
		You can also group multiple columns and then get the count:<br />
		Car.group(:model, :color)<br />
		# -> { [‘Model S’, ‘red’] => 74, [‘GTR’, ‘silver’] => 55 }<br />
		Car.select(:year).count<br />
		# -> Count of the different year values in the year column.<br />
  * Anything else?:  Not all valid select methods will work with count.  If it is invalid an error will be thrown

David Davydov

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Jasmin

  * AR Method: LIMIT
  * Description: This class method allows you to control the number of records you wish to retrieve from a table. 
  * Example: `Student.limit(2) #=> Only retrieves the first two records in the Students table`
  * Anything else?: In conjunction with `#limit`, you can also use `#offset` to specify the number of records to skip before starting to return the records. Example: `Student.limit(3).offset(30) #=> Grabs the first 3 records after skipping the first 30`

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
  
