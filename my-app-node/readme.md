// Build command => -t stands for tag
docker build -t my-first-app .

// Interactive run
docker run -it my-first-app 

// Normal run 
docker run my-first-app 

// Run with port transfer
docker run -p 3000:9000 my-first-app // where 9000 is exposed port from docker and 3000 is local port. i.e. 9000 docker port is transferred to 3000 local port

// To deploy over docker hub
docker build -t rk617605/my-first-app .     // where rk617605 is docker hub username

docker push rk617605/my-first-app

// run the pushed image
docker run -it -p 9000:9000 rk617605/my-first-app