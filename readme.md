## Docker image for testing Laravel projects

This image is based on the official PHP docker image, and uses PHP 7.

### Usage

For example in a `.gitlab-ci.yml`:

```
image: petecoop/laravel-test

test:
  cache:
    paths:
      - vendor
  script:
    - composer install --prefer-dist
    - vendor/bin/phpunit --coverage-text --colors=never
```