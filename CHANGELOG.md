# Unreleased

### Fixes

* Fix #343: Error on CLI import

### Changes

* Use composer for GetID3 package as well
* Move the composer install path from `Vendor` to `app/Vendor`

# Changes with 1.2.3

Fix a bug introduced with CakePHP 2.10 upgrade.

#### Bug / Security fixes

* Fix #342: HTTP ERROR 500 for 1.22

# Changes with 1.2.2

Fix a bug introduced with CakePHP 2.10 upgrade.

#### Bug / Security fixes

* Fix #341: /import request black-holed

# Changes with 1.2.1

This is a maintenance release with no changes for the end users.

* The CakePHP dependency is now managed with Composer (close #85)
* The documentation and the website repositories have been merged into the main
  one to simplify the maintenance
* The default CakePHP favicon is replaced by the Sonerezh icon

# Changes with 1.2.0

This new release backport stuff from the main fork of Sonerezh. A big thanks to
the community, and @gs11.

#### Bug / Security fixes:

* Merge #339: Time to merge (thanks to gs11)
* Merge #318 (fix #277): Getting "Undefined index: id [APP/Model/User.php, line
  152]" During Installation (thanks to GaneshKandu)
* Merge #312: Player now shows artist instead of band
* Merge #309: Fix related to MySQL and SQLite
* Merge #306: Upgraded CakePHP to 2.9.8 (thanks to gs11)
* Merge #304: Changed select grouping so that albums with the same name are
  listed
* Merge #300: Removed slow subquery from album view
* Merge #293: Implemented database cleaning
* Merge #287: Removed trailing slash in subdirectory path added by CakePHP for
  some folders
* Fix #263: Something wrong with files with non-latin characters in name
* Fix #241: Install script doesn't create the database
* Fix #214: Optimization: enable caching for albums covers (thanks to
  MightyCreak)
* Fix #152: IndexedDB does not function in private browsing mode (documentation
  improvement)
* Fix #107: Replace avconv with ffmpeg

Fixes from gs11's fork:

* Fixed detection of tag 'DISCNUMBER' without 'DISCTOTAL' for OGG files
* Fixed detection of disc number without a disc total in the string (e.g. '01'
  instead of '01/02')
* Fixed year not showing for album with multiple CDs

#### New features

* Merge #293: Implement database update (thanks to gs11)
* German translation (thanks to soulsymphonies)

# Changes with 1.1.3

### Bug / Security fixes:

* Revert the pull request #236 because it introduces instabilities with the database

# Changes with 1.1.2

#### New features:

* You can now download a track
* Issue #223: sort the "Albums" page by band or by album
* Issue #214: log failed authentication attempts to prevent brute-force attacks
* Issue #179 #114: pre-load next song

#### Bug / Security fixes:

* Merge #215: Playlist title cannot be empty (Thanks to disc)
* Merge #236: Fix missing albums in recently added albums (Thanks to fcharlier)
* Fix #207: Broken disc info on OGG files
* Fix #199: Improve the message on the cli tool
* Fix #196: Error on import when people mess with dates
* Fix #192: Skip symlinks on the import process to avoid infinite loops
* Fix #183: Bug if the artist string contains "$"
* Fix #180: Duplicate track on import
* Fix #178: Problem with file rights at installation
* Fix #177: Trim whitespace characters on search request
* Fix #143: Cannot choose output bitrate in conversion window
* Fix #60: Store cipherSeed and salt outside app/Config/core.php
* French translation improvements
* Other minor bugfixes
* Contributing guide

# Changes with 1.1.1

#### Bug / Security fixes:

* Fix #174: Add lock system on import process
* Fix #173: CSRF protection broke the 'add to playlist' form
* Ohter bugfixes

# Changes with 1.1.0

#### New features:

* The import function has been entirely refactored
* New CLI to import your music

#### Improvements:

* Issue #148: Upgrade CakePHP to 2.8
* Upgrade Twitter Bootstrap to 3.3.6
* Import view with debug report if warnings or errors happened
* PHP7 support

#### Bug / Security fixes:

* PRs #158 #159 #162: Typo fix (Thanks to MightyCreak,NumEricR and nodiscc)
* Fix #161: CSRF vulnerability
* Fix #155: Fatal error with getID3 lib and PHP7
* Fix #106: Too many files to import?
* Fix #51: Import bugs
* Other bugfixes

# Changes with 1.0.0

#### New features:

* Docker compatibility
* The first row on the album view shows the 6 latest albums added

#### Improvements:

* Code readability

#### Bug / Security fixes:

* Fix #142: Mp3 files without Id3 tags all showns as "Unknown"
* Fix #122: Songs are duplicated when i attempt to update database

# Changes with 1.0.0-beta2

#### New features:

* French translation (using the browser language)

Improvements:
* Improve queue behavior on the "search" view

# Changes with 1.0.0-beta

#### New features:

* #61: Set multiple root folders
* #46: Forgot my password system
* #45: Email notifications system
* #43: 'Remember Me' feature
* Sonerezh now works with PostgreSQL and SQlite (not recommended)

#### Improvements:

* Improvements on queue behavior
* #117: Port option on database installation
* #82: Improve Raspberry Pi compatibility (Thanks to kletellier)
* #72: Improve ID3v2 support
* #35: Help for get root path on shared hosting
* #32: Improve import process
* #15: Added the pointer cursor on music titles clickable lines (Thanks to maximelebastard)
* #7: Improve OGG metadata tags support
* Performance improvement in algorithm sorting

#### Bug / Security fixes:

* Fix #120: Error 500 on settings page
* Fix #73: Newly created playlists aren't listed
* Fix #48 #64: Ask for password twice when trying to update it) (Thanks to FoxiesCuties)
* Fix #34: XSS vulnerability on search form
* Fix #33: A "Listener" can update any account
* Fix #31: Do not hotlink images from flattr.com, paypalobjects.com
* Fix #23: End space in directory name
* Fix #22: Invalid search query when using history back button
* Fix #19: Unable to add songs to playlist from search results screen (Thanks to Cr33p)
* Fix #8 #71: Length path limitation (Thanks to maximelebastard)
* Fix #3: Avconv and FFmpeg
