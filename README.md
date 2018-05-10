# ( Re ) - Build & Run Elixir Only

    docker-compose -f No-db.yml up --build

If you want to start the stack as daemon , add <strong> -d </strong> 

# ( Re ) - Build & Run Elixir With Postgres and Adminer

    docker-compose -f With-db.yml up --build

If you want to start the stack as daemon , add <strong> -d </strong> 

# Create an Elixir App

    docker exec -it YOUR_ELIXIR_CONTAINER mix new .

# Get Dependencies

    docker exec -it YOUR_ELIXIR_CONTAINER mix deps.get

# Enter in Interactive Shell 

    docker exec -it YOUR_ELIXI_CONTAINER iex -S mix

</br>

# Create a Phoenix App & Start

    docker exec -it YOUR_ELIXIR_CONTAINER mix phx.new .
    docker exec -it YOUR_ELIXIR_CONTAINER mix phx.server

# Clear & Remove Volume

    docker systeme prune
    docker volume rm --force YOUR_VOLUME_NAME
    docker rmi --force YOUR_IMAGE_NAME

![index](https://github.com/Just1B/Elixir_Docker_Dev/raw/master/screen/screen.png)