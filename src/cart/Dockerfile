FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /src/cart
COPY ["*", "./"]
dotnet restore
dotnet build
ENTRYPOINT ["dotnet", "run"]
