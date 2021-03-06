# Change Log

Find all notable changes of this project in this file.

## v1.1.1 - 2020-09-28
### Fixes
- fixed getMany and getManyReferecnce for compound keys

## v1.1.0 - 2020-09-16
### Fixes
- removed requirement to define order key in react admin, when using compound keys: default was `id`, now it's the compound key

### Breaking changes
- refactored compound primary keys:
  For single custom keys wrap an array as follows:
  ```jsx
  const dataProvider = postgrestRestProvider(API_URL, fetchUtils.fetchJson, 'eq', new Map([
    ['some_table',    ['custom_id']], // <- instead of ['some_table','custom_id']
    ['another_table', ['first_column', 'second_column']],
  ]));
  ```

## v1.0.7 - 2020-08-23
### New feature
- [#14](https://github.com/raphiniert-com/ra-data-postgrest/pull/14) compound primary keys (see [README.md](https://github.com/raphiniert-com/ra-data-postgrest/blob/master/README.md#compound-primary-keys)) - @[programmarchy](https://github.com/programmarchy)

### Maintenance
- `import React from 'react';` -> `import * as React from 'react';`
- Some minor code cleanup

## v1.0.6 - 2020-06-15
### Fixes
- Fixed wrong support statement concerning [postgrest starter kit](https://github.com/subzerocloud/postgrest-starter-kit) in readme

## v1.0.5 - 2020-06-15
### Fixes
- [#13](https://github.com/raphiniert-com/ra-data-postgrest/pull/13), Remove console.log - @[jpagex](https://github.com/jpagex)
- [#12](https://github.com/raphiniert-com/ra-data-postgrest/pull/12), Fixed limit parameter - @[jpagex](https://github.com/jpagex)

## v1.0.4 - 2020-06-08
### Fixes
- Fixed missing js files in npm package [#8](https://github.com/raphiniert-com/ra-data-postgrest/issues/8)
- [#9](https://github.com/raphiniert-com/ra-data-postgrest/pull/9), Fixed typo in readme - @[seclace](https://github.com/seclace)

## v1.0.3 - 2020-05-17
### Fixes
- Fixed bug when multidelete - @[colonist4096](https://github.com/colonist4096)
- [#5](https://github.com/raphiniert-com/ra-data-postgrest/pull/6), Fixed bug while using multiple filters on the same attribute - @[olivierdalang](https://github.com/olivierdalang)

## v1.0.2 - 2020-03-10
### Fixes
- [#4](https://github.com/raphiniert-com/ra-data-postgrest/pull/4), Fixed bug while using ReferenceField with UUID - @[xero88](https://github.com/xero88)

## v1.0.1 - 2020-02-01
- initial release
