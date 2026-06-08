# Magento 2.4.9 / PHP 8.5 Compatibility

This fork updates `ethanyehuda/magento2-cronjobmanager` for Magento 2.4.9 / PHP 8.5.

## Changes

- Added PHP 8.5 to the Composer PHP constraint.
- Added Symfony Console 7.4 to the Composer constraint.
- Added `: int` return type to Symfony Console command `execute()` methods where needed.
- Scanned for PHP 8.4/8.5 implicit nullable parameter issues.
- Scanned for Magento 2.4.9 `system.xml` inline comment compatibility issues.

## Usage

Add this fork as a VCS repository in your Magento project's `composer.json`, then require the branch alias.

## Testing

Recommended tests:

```bash
composer validate --strict
php bin/magento setup:upgrade
php bin/magento module:status EthanYehuda_CronJobManager
php bin/magento cronmanager:showjobs
php bin/magento cronmanager:runjob some_job_code
```
