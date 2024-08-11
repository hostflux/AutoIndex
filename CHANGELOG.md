# AutoIndex PHP Script

## Change Log

**Legend**:  
(+) Added feature  
(!) Security bug fixed  
(-) Bug fixed  
(\*) Improved/changed feature  
( ) Non-code change

### [AutoIndex PHP Script](https://github.com/hostflux/AutoIndex), by [Hostflux LLC](https://hostflux.com)

**Version 2.2.4 revision 2** (2021-Jun-04)  
(+) Added support for PHP 8.0.x and higher

**Version 2.2.4 revision 1** (2018-Nov-13)  
(+) Added support for PHP 7.0.x and higher

### [AutoIndex PHP Script](https://github.com/justinhagstrom/AutoIndex), by [Justin Hagstrom](http://autoindex.sourceforge.net)

**Version 2.2.4** (2007-Nov-09)  
(!) Fixed DOS bug  
( ) Added Vista icon set

**Version 2.2.3** (2007-Nov-05)  
(!) Fixed XSS bug

**Version 2.2.2** (2007-Jul-24)  
(!) Fixed XSS bug in search feature

**Version 2.2.1** (2007-Jan-06)  
(\*) Improved handling of passwords with .htaccess  
(\*) Improved default stylesheet  
( ) Added Danish translation  
( ) Updated Dutch translation

**Version 2.2.0** (2006-Jan-02)  
(+) Added a pagination feature  
(+) Language is selected based on the user's browser's default  
(+) Added support for PHP 5.1.x and higher  
( ) Added Greek and Japanese translations

**Version 2.1.2** (2005-Aug-11)  
(-) Fixed bug when editing descriptions of filenames that have special characters  
( ) Added Czech and Slovak translations

**Version 2.1.1** (2005-Jul-06)  
(!) Fixed bug with search box  
( ) Added Swedish translation

**Version 2.1.0** (2005-Feb-14)  
(+) Added a .htaccess parser  
(+) Added an FTP browser  
(+) Added _moderator_ and _banned_ account levels  
(+) Added a feature to let moderators/admins change their own password

**Version 2.0.7** (2005-Jan-14)  
(-) Fixed _file\_description_ feature

**Version 2.0.6** (2005-Jan-04)  
(+) Admins are able to copy files from other servers (similar to "wget")  
( ) Added Thai and Arabic translations

**Version 2.0.5** (2004-Sep-02)  
(+) When _force\_download_ is on, the MIME-type sent depends on the file extension  
(\*) Using _hidden\_files_ to only show certain files no longer restricts directories

**Version 2.0.4** (2004-Aug-17)  
(\*) When reconfiguring the script, the current settings are selected instead of the defaults  
( ) Added Polish translation

**Version 2.0.3** (2004-Jul-26)  
(\*) Nested if-statements can be used in the template files  
(\*) Folders do not have to be empty to be deleted

**Version 2.0.2** (2004-Jul-13)  
(\*) All output is XHTML 1.1 compliant  
(\*) The _do\_every_ template command now does not include the last file listed

**Version 2.0.1** (2004-Jul-05)  
(+) Added directory cache feature  
(\*) Added _include_ command to the template system  
(-) Fixed search page bug when _download\_count_ was on

**Version 2.0.0** (2004-Jun-24)

Complete rewrite from version 1.0:

*   Now uses PHP 5. PHP version 5.0 or higher is required.
*   All the features of version 1, plus:  
    (+) Has a template system for all HTML output  
    (+) Tar archives of directories can be downloaded  
    (+) Each user account can have its own home directory  
    (\*) Passwords are stored as a sha-1 hash rather than md5 (this is slightly more secure)
