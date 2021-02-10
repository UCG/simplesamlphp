#Information About This Fork

##General

When merging in changes from new versions in this fork, care must be taken to ensure the `SimpleSAML\Module\drupalauth\PreDrupalBootEnvironment` class in the drupalauth module is
compatible with the new version of simpleSAMLphp.

##Changes

- A new method was added to the `SimpleSAML\Auth\Source` class, `SimpleSAML\Auth\Source::executeLogoutTasksWhenUnauthenticated`. This class is called by
`SimpleSAML\Auth\Simple::logout` to give authentication sources a chance to perform
logout tasks even if there is no simpleSAMLphp session.