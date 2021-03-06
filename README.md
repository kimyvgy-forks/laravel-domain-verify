# sun-asterisk/laravel-domain-verify

Verify domain ownership for the Laravel application. We provide three ways to verify the domain (like Google):

- [ ] Via domain's DNS record (txt record)
- [ ] Via HTML tag
- [ ] Via Adminstrator's email address. Supported: `admin@domain.example` and `webmaster@domain.example`.

## Installation

First, install Domain Verifier via the Composer package manager:

```bash
composer require sun-asterisk/laravel-domain-verify
```

After that, you need to add provider `DomainVerifierServiceProvider` in `config/app.php`.
Now, you should publish the Domain Verifier configuration and migration via `artisan` command:

```bash
php artisan vendor:publish --provider="SunAsterisk\DomainVerifier\DomainVerifierServiceProvider"
```

If you just want to publish only configuration or migrations:

```bash
php artisan vendor:publish --provider="SunAsterisk\DomainVerifier\DomainVerifierServiceProvider" --tag=config
php artisan vendor:publish --provider="SunAsterisk\DomainVerifier\DomainVerifierServiceProvider" --tag=migrations
```

## Requirements

- Laravel `>= 5.6.0`
