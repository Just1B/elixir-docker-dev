# ( Re ) - Build & Run Elixir Only

    docker-compose -f docker-compose-nodb.yml up --build

If you want to start the stack as daemon , add <strong> -d </strong> 

# ( Re ) - Build & Run Elixir With Postgres and Adminer

Edit de `.env` file and :

    docker-compose -f docker-compose-db.yml up --build

If you want to start the stack as daemon , add <strong> -d </strong> 

# Create an Elixir App

    docker exec -it YOUR_ELIXIR_CONTAINER mix new .

# Get Dependencies

    docker exec -it YOUR_ELIXIR_CONTAINER mix deps.get

# Enter in Interactive Shell 

    docker exec -it YOUR_ELIXI_CONTAINER iex -S mix

</br>

# Create a Phoenix App & Start

You can pass the `--no-brunch --no-html` to `mix phx.new . ` for API only

    docker exec -it YOUR_ELIXIR_CONTAINER mix phx.new .

Now edit `app/config/dev.exs` => hostname: "postgres" in the database section and :

    docker exec -it YOUR_ELIXIR_CONTAINER mix phx.server

# Clear & Remove Volume

    docker systeme prune
    docker volume rm --force YOUR_VOLUME_NAME
    docker rmi --force YOUR_IMAGE_NAME

![index](https://github.com/Just1B/Elixir_Docker_Dev/raw/master/screen/screen.png)

# Ressources

    - https://devhints.io/phoenix-ecto
    - https://lobotuerto.com/blog/building-a-json-api-with-phoenix-and-elixir/

# Licence

The MIT License

Copyright (c) 2018 JUST1B

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
