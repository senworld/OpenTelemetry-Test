FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /src/cart
COPY ["/src/*", "/src/cart/"]
RUN dotnet restore
RUN dotnet build
ENTRYPOINT ["dotnet", "run"]
