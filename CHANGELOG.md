# Release Notes for Webhooks for Craft CMS

## Unreleased

### Added
- Webhook URLs can now be set to environment variables or Twig code. ([#18](https://github.com/craftcms/webhooks/issues/18))

## 2.2.0 - 2019-07-29

### Added
- Webhooks can now specify custom request headers. ([#12](https://github.com/craftcms/webhooks/issues/12))

## 2.1.0 - 2019-07-26

### Added
- Webhooks for element events can now be executed depending on whether the element is new, is a draft/revision, or is being duplicated/propagated/bulk-resaved. ([#14](https://github.com/craftcms/webhooks/issues/14))
- Modules and plugins can register additional webhook filters using the new `craft\webhooks\Plugin::EVENT_REGISTER_FILTER_TYPES` event.  

### Fixed
- Fixed an error that could occur when detecting available component classes in Craft 3.2.

## 2.0.1 - 2019-03-20

### Fixed
- Fixed a bug where it wasn’t possible to create or edit webhooks if a plugin contained an invalid class. ([#8](https://github.com/craftcms/webhooks/issues/8))
- Fixed a SQL error that would occur on installs that had been updated from Webhooks 1.x.
- Fixed a SQL error that occurred when attempting to uninstall Webhooks.

## 2.0.0 - 2019-03-19

### Added
- Webhooks now logs requests, and it’s possible to view them from a new “Activity” page within the plugin.
- Added new `maxDepth`, `maxAttempts` and `attemptDelay` settings, which can be set from `config/webhooks.php`.
- The Sender Class and Event Name webhook settings now show suggestions based on the available classes and events.
- Webhooks can now have custom payloads. ([#3](https://github.com/craftcms/webhooks/pull/3))

### Changed
- Webhooks now requires Craft 3.1 or later.

## 1.1.2 - 2018-12-21

### Changed
- Webhook requests now include data for any magic event properties defined by `fields()`, if the event class implements `yii\base\Arrayable`. ([#2](https://github.com/craftcms/webhooks/issues/2))   

## 1.1.1 - 2018-12-17

### Added
- Webhooks is now translated into Chinese. ([#1](https://github.com/craftcms/webhooks/pull/1))

### Fixed
- Fixed a bug where the “Extra User Attributes”, “Extra Sender Attributes”, and “Extra Event Attributes” fields were visible when editing an existing webhook with a GET request method.

## 1.1.0 - 2018-12-13

### Added
- Added support for webhooks that send GET requests.
- Webhook names and group names can now contain emojis, even if using MySQL.
- Typing `->` or `=>` into a webhook’s Name field now creates a ➡️.  

## 1.0.1 - 2018-12-13

### Fixed
- Fixed a bug where webhook-send jobs didn’t have descriptions.

## 1.0.0 - 2018-12-13

Initial release.
