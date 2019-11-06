#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see http://aka.ms/containercompat 

#FROM microsoft/iis/dotnet:2.1-sdk-nanoserver-1809
FROM mcr.microsoft.com/dotnet/framework/sdk:4.7.2-windowsservercore-ltsc2019
ARG source
COPY ${source:-obj/Docker/Publish} /inetpub/wwwroot
#CMD ["C:\\ServiceMonitor.exe", "w3svc"]
#./publish .

