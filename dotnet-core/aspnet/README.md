# Dotnet Core Sample App using ASPNet

## Building

`pack build aspdotnet --builder vk-builder:bionic --path /Users/vamshikyadav/Documents/code/buildpacks/dotnet-core/aspnet`

## Running

`docker run --interactive --tty --env PORT=8080 --publish 8080:8080 dotnet-aspnet-sample`

## Viewing

`curl http://localhost:8080`
