FROM mcr.microsoft.com/dotnet/aspnet:8.0
WORKDIR /app

COPY build/ .
EXPOSE 8001

ENTRYPOINT ["dotnet", "Auth-Microservice.dll"]