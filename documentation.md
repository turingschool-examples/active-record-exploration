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

  * AR Method: Sum
  * Description: Sum calculates the sum of all values on a given column, and will return the same datatype of these values 
  * Example: Company.sum(:revenue) => 100000
  * Anything else?: If there is no row in the column (i.e. no data), the method will return 0

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

  * AR Method: 	`save`
  * Description: This method creates an already existing object in the database. It returns false if it wasn't able to be created, possibly because of failed validations like `presence: true`.
  * Example: 
  ```ruby
  Student.all.count => 0
  s1 = Student.new(name: 'bob')
  s1.save => true
  s2 = Student.new
  s2.save => false
   ```bob = Student.new; bob.save
  * Anything else?: `create` is the same as `new` and `save`. `new` makes the object, and `save` saves it in the actual database.

Jasmin

  * AR Method: LIMIT
  * Description: This class method allows you to control the number of records you wish to retrieve from a table. 
  * Example: `Student.limit(2) #=> Only retrieves the first two records in the Students table`
  * Anything else?: In conjunction with `#limit`, you can also use `#offset` to specify the number of records to skip before starting to return the records. Example: `Student.limit(3).offset(30) #=> Grabs the first 3 records after skipping the first 30`

Jean

  * AR Method: Order
  * Description: Order will order a collection according to the value of the specified attribute
  * Example:
   *  `Student.order('name')` is the same as `Student.order(:name)`, both order by the value of name
   *   `Student.order('created_at DESC')` is the same as `Student.order(created_at: :desc)`, both order by the value in the specified ascending/descending order
  * Anything else?:
   *  ordering by letters will order alphabetically, while ordering numbers will order numerically. You can also chain ordering - e.g. `Student.order(:name).order(updated_at: :asc)` will order first alphabetically by name then by ascending update time

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

  * AR Method: Distinct
  * Description: Specifies whether the record returned should be unique or not.
  * Example: Teacher.select(:name) <= Might return two records with the same name
             Teacher.select(:name).distinct <= Returns one record per distinct name
  * Anything else?: You can also remove the uniqueness by placing two distincts consecutively and placing false in parens 
  at the end. ex. Teacher.select(:name).distinct.distinct(false)

Raphael

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:

Ryan

  * AR Method: includes
  * Description: Class method allowing a user to call only the columns with a specified attribute.
  * Example: 
```ruby
@companies = Company.includes(:persons).where(:persons => { active: true } ).all
 
@companies.each do |company|
     company.person.name
end
```
  * Anything else?: This method is similar to joins, but as the Rails docs states, includes loads the specified associations using a minimal amount of queries.  This, in turn, leads to better performance than joins.

Sonia

  * AR Method: take
  * Description: It returns an array containing a specificed number or default number of objects from a class. The array is not necessarily in a particular order.
  * Example: `PayloadRequest.take` returns an array containing one `PayloadRequest` object, the first one created. `PayloadRequest.take(5)` returns the first five objects in the collection, but not necessarily in order.
  * Anything else?: It is important to distinguish between .take and .limit. The latter returns an ActiveRecord relation which means you can chain more methods to it, unlike with .take.

Susi

  * AR Method: 
  * Description:
  * Example:
  * Anything else?:
  
