FROM jousby/amazon-openjdk

# Add the elastic search repo to yum's known sources
RUN { \
        echo '[elasticsearch-5.x]'; \
        echo 'name=Elasticsearch repository for 5.x packages'; \
        echo 'baseurl=https://artifacts.elastic.co/packages/5.x/yum'; \
        echo 'gpgcheck=1'; \
        echo 'gpgkey=https://artifacts.elastic.co/GPG-KEY-elasticsearch'; \
        echo 'enabled=1'; \
        echo 'autorefresh=1'; \
        echo 'type=rpm-md'; \
    } > /etc/yum.repos.d/elasticsearch.repo

# Install latest elasticsearch package via yum
RUN set -x \
    && rpm --import https://artifacts.elastic.co/GPG-KEY-elasticsearch \
    && yum -y install elasticsearch \
    && chkconfig --add elasticsearch
