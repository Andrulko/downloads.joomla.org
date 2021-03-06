# Joomla! Downloads Portal

This repository holds additions from the base Joomla! application (extensions, layouts, etc.) for the Joomla! Downloads Portal.

## Akeeba Release System

The site is primarily powered by [Akeeba Release System](https://github.com/akeeba/release-system) with custom frontend layouts. However, there are also some modifications to the component:

- The `Akeeba\ReleaseSystem\Admin\Model\Releases` class has an added `announcement_url` property (and accompanying SQL change) to allow a URL to the release post to be used
- The `Akeeba\ReleaseSystem\Site\Helper\DownloadCounter` class has been added to help query download counts (primarily for use on the homepage and the admin dashboard)
- The frontend router has been modified to allow an item to be routed via its filename or alias (primarily used for download stream URLs)
- The frontend router has been modified to throw a 404 versus falling back to ARS' native repository view
- The `plgContentArslatest` class has been modified to support two additional shortcodes: `release_announcements` and `vgroup_downloads`
