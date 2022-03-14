# FROM microsoft/dotnet:2.0.0-sdk
FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/Worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 

CMD dotnet src/Worker/Worker.dll