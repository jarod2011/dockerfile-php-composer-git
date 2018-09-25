FROM php:cli
MAINTAINER xinghen249@gmail.com

RUN cd / && mkdir www conf shell \
    && cd / && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php --install-dir=/usr/bin/ --filename=composer \
    && chmod +x /usr/bin/composer \
    && curl -o /usr/local/bin/gitlab-runner https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-linux-amd64 \
    && chmod +x /usr/local/bin/gitlab-runner \
    && useradd --comment 'GitLab Runner' --create-home gitlab-runner --shell /bin/bash \
    && gitlab-runner install --user=gitlab-runner --working-directory=/home/gitlab-runner \
    && chown -R gitlab-runner /shell \
    && apt-get update && apt-get install -y git

COPY entry.sh /conf/

CMD [ "bash" "/entry.sh" ]
