FROM alpine AS build
WORKDIR /src/cart
COPY ["/src/*", "/src/cart/"]
RUN apk add curl
RUN curl -L https://dot.net/v1/dotnet-install.sh -o dotnet-install.sh
RUN chmod +x ./dotnet-install.sh
RUN ./dotnet-install.sh --version latest
RUN export DOTNET_ROOT=$HOME/.dotnet
RUN export PATH=$PATH:$DOTNET_ROOT:$DOTNET_ROOT/tools
RUN dotnet restore
RUN dotnet build
ENTRYPOINT ["dotnet", "run"]
