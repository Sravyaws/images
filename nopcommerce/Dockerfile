FROM mcr.microsoft.com/dotnet/sdk:7.0
LABEL author="sravya" organization="qt" project="learning"
ARG user=nopcom
ARG group=nopcom
ARG uid=1000
ARG gid=1000
WORKDIR /nop
RUN apt update && apt install unzip -y
RUN groupadd -g 1000 nopcom \
    && useradd -d "/nop" -u ${uid} -g ${gid} -m -s /bin/bash ${user}
ADD --chown=nopcom:nopcom https://github.com/nopSolutions/nopCommerce/releases/download/release-4.60.2/nopCommerce_4.60.2_NoSource_linux_x64.zip /nop/nopCommerce_4.60.2_NoSource_linux_x64.zip
RUN unzip /nop/nopCommerce_4.60.2_NoSource_linux_x64.zip && \
    mkdir /nop/bin && mkdir /nop/logs
EXPOSE 5000
CMD [ "dotnet", "Nop.Web.dll","--urls", "http://0.0.0.0:5000"]