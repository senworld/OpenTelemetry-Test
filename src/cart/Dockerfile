FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /src/cart
COPY ["*", "/src/cart/"]
RUN dotnet restore cart.csproj
RUN dotnet build cart.csproj -c Release -o /app/build
ENTRYPOINT ["dotnet", "run", "--project", "cart.csproj"]
