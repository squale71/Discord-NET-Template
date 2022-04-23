#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app

FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /src
COPY ["Discord NET Template/Discord NET Template.csproj", "Discord NET Template/"]
RUN dotnet restore "Discord NET Template/Discord NET Template.csproj"
COPY . .
WORKDIR "/src/Discord NET Template"
RUN dotnet build "Discord NET Template.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Discord NET Template.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Discord NET Template.dll"]
