FROM dotnet:6.0 AS build
WORKDIR /src/cart
COPY ["*", "./"]
dotnet restore
dotnet build
ENTRYPOINT ["dotnet", "run"]
