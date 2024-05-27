- Docker command for mongo (./)
  docker run -d --name mongo_c --rm -e MONGO_INITDB_ROOT_USERNAME=hubla_goals_username -e MONGO_INITDB_ROOT_PASSWORD=hubla_goals_password --network goals_n -v goals_db:/data/db mongo

- Docker command for BE (./BE)
  build : docker build -t hubla/goals_be .
  run : docker run -it -v $(pwd):/app -v logs:/app/logs -v app/node_modules -p 80:80 --network goals_n --name goals_be_c hubla/goals_be

- Docker command for FE (./FE)
  build: docker build -t hubla/goals_fe .
  run : docker run -it -v $(pwd)/src:/app/src --name goals_fe_c -p 3000:3000 hubla/goals_fe
