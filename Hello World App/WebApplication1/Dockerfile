#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see http://aka.ms/containercompat 
#FROM microsoft/aspnet:4.7.2-windowsservercore-1803
FROM microsoft/dotnet:2.1-sdk-nanoserver-1809
RUN Add-WindowsFeature Web-Server;
RUN Add-WindowsFeature NET-Framework-45-ASPNET;
RUN Add-WindowsFeature Web-Asp-Net45;
ARG source
#WORKDIR 
COPY ${source:-obj/Docker/Publish} /inetpub/wwwroot
CMD ["C:\\ServiceMonitor.exe", "w3svc"]
#./publish .

