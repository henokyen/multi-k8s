from node:alpine as builder 
workdir '/app'
copy ./package.json ./
run npm install 
copy . .


#set up the actual build process, the step that actually builds the production version of our frontend and assets
# the output from this step will be a folder inside of that '/app' directory called build.
#That's where all the production assets get placed.
run npm run build 

from nginx

#we are replacing the default.conf file which exists in the nginx image
expose 3000

#replace the default.conf file which exists in the nginx image by the one defined in the ./nginx directory inside the client directory
copy ./nginx.default.conf /etc/nginx/conf.d/default.conf 

#now copy over the production version of all of our assets 
#that reside inside the '/app/build into a place where nginx serves front-end pages

copy --from=builder /app/build /usr/share/nginx/html
