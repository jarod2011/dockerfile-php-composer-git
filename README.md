dockerfile-php-composer-git
-----
a php environment with gitlab runner and composer

Docker Link: [jarod2014/php-composer-gitlab-runner](https://hub.docker.com/r/jarod2014/php-composer-gitlab-runner/)

### how to use it ?
```bash
docker pull jarod2014/php-composer-gitlab-runner
```

### tags
* latest: this images use based by php:cli
* phpfpm: this images used based by php:fpm

### entry script (only cli)
```bash
/conf/entry.sh
```

### gitlab-runner script path (this directory owner is gitlab-runner)
```bash
/shell/
```
