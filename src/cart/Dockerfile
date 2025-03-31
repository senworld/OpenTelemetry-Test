FROM okteto/dotnetcore:8.0 AS build
WORKDIR /src/cart
COPY ["/src/*", "/src/cart/"]
RUN dotnet restore
RUN dotnet build
ENTRYPOINT ["dotnet", "run"]
