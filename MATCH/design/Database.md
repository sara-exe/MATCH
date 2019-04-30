- Data stored for every user
  - username (string)
  - userdisplayname (string)
  - userpassword (string)
  - usermaxtraveldistance (double) (what is this? miles?)
  - userlatitude (double)
  - userlongitude (double)
  - aboutMe/Bio (string)
  - Hobbies (15 bit binary string representing the following preset hobbies)
    - Swimming 
    - Reading  
    - Bicycling 
    - Hiking 
    - Camping  
    - Dancing  
    - Running  
    - Bowling 
    - Video Games   
    - Programming  
    - Reading  
    - Watching TV   
    - Going to the Movies       
    - Basketball 
    - Football

### Methods

- createSchema
  - connects to mysql, creates the db and table if it doesn't exist
- userLogin
  - Takes in strings name and password
  - Outputs Boolean (true if login success, false if failure)
- getDisplayName, getPassword, getAboutMe, getHobbies, getMaxTravelDistance, getLatitude, getLongitude
  - Takes in strings username
  - Outputs a String or double with the corresponding property of that user in the db
- getUserList
  - Outputs an ArrayList of all the username strings in the db
- createUser
  - Input
    - strings
      - username
      - password
      - displayName
      - aboutMe
      - hobbies
    - doubles
      - maxTravelDistance
      - latitude
      - longitude
  - Output boolean