
Matt
* AR Method:
### find_or_create_by(attributes, &block)

* Description:
#### Finds the first record with the given attributes or creates the record with the attributes if the record is not found

* Example:

#### Say we have a table of singers with columns first_name, last_name, and genre

    Singer.find_or_create_by(first_name: 'Taylor', genre: 'Pop')
      # => #<Singer id: 1, first_name: 'Taylor', last_name: nil, genre: 'Pop'>
    Singer.find_or_create_by(first_name: 'Elvis')
      # => #<Singer id: 2, first_name: 'Elvis', last_name: nil, genre: nil>

#### Will create a new singer if you do not validate the fields

    Singer.find_or_create_by(genre: 'Pop')
      # => #<Singer id: 1, first_name: 'Taylor', last_name: nil, genre: 'Pop'>
    Singer.find_or_create_by(genre: 'Rock')
      # => #<Singer id: 3, first_name: nil, last_name: nil, genre: 'Rock'>
      
#### Can run a block as well

    Singer.find_or_create_by(first_name: 'Justin') do |singer|
        singer.last_name = 'Bieber'
        singer.genre = 'Pop
    end
      # => #<Singer id: 4, first_name: 'Justin', last_name: 'Bieber', genre: 'Bad'>
      
* Anything Else?:

####If you don't have your fields validated on creation, it will create attributes with nil values as long as it doesn't find the attributes you pass in. 

#### To validate authenticity, you would have to run all attributes through as arguments.

#### Only returns one object.  The first one if finds, so if you are running a block, it will only update one record.
