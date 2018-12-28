from node:alpine
workdir "/app"
copy ./package.json ./
run npm install
copy . .
cmd ["npm", "run", "start"] #define a startup command, this part is different from the Dockerfile.dev file
# remember all the comamnds defined here are specified in the package.json files. that is make usre you have start command inside the package.json file