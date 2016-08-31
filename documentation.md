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
  * AR Method: having
    * Description: Having is always used in conjuction with group. Think of it as "group where." (Note that where cannot be called after group, hence the need for a different method).
  * Example: 
    * Find all products for which the price is the same as at least 4 other products. Said another way, group all products by their price, then count how many items share the same prices, then return only the collections of products for which that count is 5 or more. So group by price where that count is greater than 4.
    * `Product.group(:price).having("count(price) > 5")`
  * Anything else?:
    * Input: result of a group query (an ActiveRecord object)
    * Output: new ActiveRecord object with a collection of elements matching the group/having combination.

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
  
