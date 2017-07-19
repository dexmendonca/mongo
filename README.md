# criar usuário normal
use dbnome

var user = {
  "user" : "website",
  "pwd" : "abc123",
  roles : [
      {
          "role" : "readWrite",
          "db" : "dbnome"
      }
  ]
}

db.createUser(user);

exit
# criar usuário admin

db.createUser(
   {
       user: "user", 
       pwd: "password", 
       roles:[{role:'root', db:'admin'}]
   })
   
 # URI funcionando
 
 mongodb://user:password@host:port/db?authSource=admin
