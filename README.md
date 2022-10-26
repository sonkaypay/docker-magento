# Magento development environment

Reference: https://github.com/markshust/docker-magento

## Getting started

```bash
bin/download 2.4.5
bin/setup magento.test

bin/magento module:disable Magento_TwoFactorAuth
bin/magento sampledata:deploy
bin/magento setup:upgrade
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

## Clean up

```bash
bin/removeall
```
