FROM microsoft/dotnet

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/ \
    && dotnet publish -c Release -o ./ src/Worker/ \
    && rm -rf src/ $HOME/.nuget/

CMD dotnet Worker.dll