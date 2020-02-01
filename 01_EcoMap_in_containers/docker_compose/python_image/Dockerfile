FROM python:2
WORKDIR /usr/src/EcoMap
COPY requirements.txt ./
RUN set -eux; \
    apt-get dist-upgrade -y; apt install -y wget; \
    wget https://dev.mysql.com/get/mysql-apt-config_0.8.14-1_all.deb; \
    dpkg -i ./mysql-apt-config_0.8.14-1_all.deb; apt install -f -y; \
    apt search mysql; \
    pip install --no-cache-dir -r requirements.txt