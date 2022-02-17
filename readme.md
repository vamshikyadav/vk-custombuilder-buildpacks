# Custom builder end to end easy understanding

## Custom Stack

* Creating a custom stack allows you to configure the base images for the build-time environment for your builder and the run-time for your application.
    * you can use dockerfiles to create build-time and run-time stack
        * docker build -f dockerfile.base -t cnbs/vamshi-stack-base:bionic --target base .
        * docker build -f  dockerfile.run -t cnbs/vamshi-stack-run:bionic --target run .
        * docker build -f dockerfile.buil -t cnbs/vamshi-stack-build:bionic --target build .

## custom builder

* Creating a custom builder allows you to control what buildpacks are used and what image apps are based on.
    * Use the sample builder.toml file to create the your own builder with stack created above
        * pack builder create vk-builder:bionic --config ./builder.toml

## Building application Gradle, maven, dotnet, ruby and golang
* We can use our builder to build an app by running below commands
    * pack build aspdotnet --builder vk-builder:bionic --path /dotnet-core/aspnet
    * pack build kotlin --builder vk-builder:bionic --path /kotlin 
    * pack build maven --builder vk-builder:bionic --path /maven
    * pack build goexample --builder vk-builder:bionic --path /example-go/hello/
