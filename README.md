# Magento development environment

Reference: https://github.com/markshust/docker-magento

## Getting started

```bash
bin/download 2.4.5
bin/setup magento.test

bin/magento module:disable Magento_TwoFactorAuth
bin/magento sampledata:deploy
bin/magento setup:upgrade

bin/magento deploy:mode:set developer
```

## Usage

### Start

```bash
bin/start
```

### Admin login

- https://magento.test/admin/
- `john.smith`
- `password123`

### Kaypay Module

```bash
git clone git@gitlab.com:kaypay-oss/php-magento2-module.git

# install dependencies
bin/composer require kaypay/sdk
bin/copyfromcontainer --all 

# uncomment the volume mapping in ./docker-compose.dev.yml
# then restart the containers
bin/start

# follow installation steps from module's README
bin/magento setup:upgrade
bin/magento setup:di:compile
bin/magento cache:clean
```

## Clean up

```bash
bin/removeall
```
