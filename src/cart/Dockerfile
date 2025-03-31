FROM alpine AS build
WORKDIR /src/cart
COPY ["*", "/src/cart/"]
RUN apk add bash curl libstdc++
RUN curl -L https://dot.net/v1/dotnet-install.sh -o dotnet-install.sh
RUN chmod +x ./dotnet-install.sh
RUN ./dotnet-install.sh --version latest
RUN /root/.dotnet/dotnet restore
RUN /root/.dotnet/dotnet build
ENTRYPOINT ["dotnet", "run"]
