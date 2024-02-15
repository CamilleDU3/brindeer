
# Video
If instructions below are unclear a video is available in the repository (demo.mp4)

# Instructions

-first delete images related to this project 
-then do the following commands :

commands : 
cd brindeer-common
docker build . -t brinder-common
cd ..
docker compose up -d
docker network create kong-net

-before trying the swagger
 -add in keycloak the users

-before trying /matches
 -create a profil (/profiles) and add its location (/locations/update)
 -add in brinder/userLocation a new index with value in index field 'location' and in type 2dsphere
 https://www.mongodb.com/try/download/compass

# Remark
When calling /profiles/current we use the fact that the user is logged in keycloak 
(has an account in keycloak)
 to register a new account in mongodb directly 
 using the information from the jwt generated by keycloak 
