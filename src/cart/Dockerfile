FROM alpine AS build
WORKDIR /src/cart
COPY ["*", "/src/cart/"]
RUN apk add bash curl libstdc++ icu libgcc 
RUN curl -L https://dot.net/v1/dotnet-install.sh -o dotnet-install.sh
RUN chmod +x ./dotnet-install.sh
RUN ./dotnet-install.sh --version latest
RUN /root/.dotnet/dotnet restore cart.csproj
RUN /root/.dotnet/dotnet build cart.csproj
ENTRYPOINT ["dotnet", "run"]
