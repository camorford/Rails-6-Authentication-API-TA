# README

testing: 

1) Create a user :
  - User.create!(email: 'example@mail.com', password: '1234', password_confirmation: '1234')
  
2) curl : 
    curl -H "Content-Type: application/json" -X POST -d '{"email":"example@mail.com", "password":"1234"}' http://localhost:3000/authenticate
    { receive auth token } 
    
With Auth: 

  curl -H "Authorization: #{auth_token}" http://localhost:3000/items
  
  
Without Auth (receive an error) 

  curl  http://localhost:3000/items
