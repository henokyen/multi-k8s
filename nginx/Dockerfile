From nginx:latest

#we are replacing the default.conf file which exists in the nginx image
copy ./default.conf /etc/nginx/conf.d/default.conf 

#note:
 #there is no command to run because
 #remember that if we do not replace the default command of an image inside of the docker file then the default
 #command of the parent image which is from nginx right here will automatically take precedence.
