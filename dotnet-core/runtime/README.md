# Dotnet Core Sample App using Runtime only

## Building

`pack build aspdotnet --builder vk-builder:bionic --path /dotnet-core/aspnet`

## Running

`docker run --interactive --tty --env PORT=8080 --publish 8080:8080 dotnet-runtime-sample`

## Viewing

`curl http://localhost:8080`
