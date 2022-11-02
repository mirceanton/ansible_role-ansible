# Changelog

## v2.0.1

* Changed the `ansible_apt_additional` and `ansible_apt_additional` to be a simple list of packages instead of `{name: <package_name>}`.
* Fixed `ansible_apt_additional` and `ansible_apt_additional` getting overwritten by default vars.

## v2.0.0

**💣 Breaking changes**:

* Changed variable names so that all of them are prefixed by `ansible_`

**🔧 Workflow changes**:

* Migrated grom `geerlingguy/` images to custom `antonmircea/` images
* Added testing support for more platforms

## v1.0.0

* Initial release of the `mirceanton.ansible` role 🚀
