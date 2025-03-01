Oxwall 1.9.0, February 20, 2023
====================================

Platform[core]:
- php 8 support
- removed mobile version support
- fixed terms of use and privacy policy pages could not be viewed on complete profile
- added the possibility to pass a static id for a form element when creating it
- removed fake elements on forms
- fixed url validation error when creating static pages
- fixed admin side menu elements padding in firefox browser
- fixed date range dynamic update for the Date form element
- prevent floatbox from closing when click outside of active window area

Oxwall 1.8.4, July 26, 2016
====================================

Platform [core]:
- added advanced SEO settings for site pages 
- added option to generate and update sitemap
- removed hardcode for Submit form element (contributed by revkov https://github.com/oxwall/oxwall/pull/357)
- made the reason for a profile suspension displayable on site
- fixed preloader display for Simplicity theme
- introduced hardcode ban to upload PHP files
- introduced required PHP version check before platform update 
- when attempting to update plugins while there is an available platform update present, the system will warn admins to perform platform update first
- fixed the display order for profile fields on profile view page within mobile version
- changed URL attribution to https://developers.oxwall.com
- changed anti-CSFR token lifetime to match user’s on-site session time
- fixed avatar crop bug on profile edit page
- improved SSL integration with CloudFlare

Forum [forum]:
- fixed display of quoted text for Simplicity theme (contributed by WalterMisar https://github.com/oxwall/simplicity/pull/7)

Advertisement [ads]:
- fixed fatal error during plugin installation

Videos [video]:
- fixed integration with dailymotion.com


Oxwall 1.8.3, May 17, 2016
====================================

Platform [core]:
- added CURL support for remote platform requests
- added blocked users list
- fixed message appearing during theme upload with missing update server connection
- added option to use empty database user password during installation
- fixed bug preventing cash clearing for configs during single script launches
- added standard placeholder for forms, which displays invalid label
- added Check Updates button to Admin Panel for manual update checks
- added ALT HTML attribute for profile avatars on profile list page
- added support for anti CSFR tokens, which are now used by all forms automatically. Individual usage access is also available. 
- removed send escaper functions
- fixed mobile version bug preventing login from any page
- removed .htaccess file from update pack
- fixed bug with inverted commas within langs breaking stats on Admin Panel index page

Photos [photo]:
- photo description is no longer cut due to tag presence
- added ALT HTML attribute for photo thumbs within photo widget on profile view page, as well as photo lists (latest, top rated, most discussed)
- added ALT HTML attribute for photos on separate photo view page
- added GET parameter for temporary photos to prevent caching errors

Newsfeed [newsfeed]:
- added ALT HTML attribute for displaying thumbs of various content

Messages [mailbox]:
- blocked users no longer show up in contact list
- contact list search now displays results with partially typed-in names
- fixed bug with invitation label not disappearing in chat window
- fixed JS error “TypeError: element.input is null" appearing while switching operation modes (chat/mail/chat+mail) in plugin settings

Video [video]:
- added ALT HTML attribute for video thumbs on video listings page

Events [event];
- added ALT HTML attribute for event thumbs

Groups [groups]:
- added ALT HTML attribute for group thumbs


Oxwall 1.8.2, Mar 22, 2016
====================================

Platform [core]:
- oxwall minimum PHP supported version increased to 5.5;
- the list of changes is now shown during plugin update request (if the plugin developer added the list of changes to the Store);
- improved validation system for commercial plugins/themes;
- added new class definition <body class="ow {$theme-name}"> for each theme, where $thene-name is taken from theme.xml
- fixed several XSS vulnerabilities (thanks to a report from Tim Coen);
- added Uninstall option for disabled plugins in the Admin Panel;
- fixed a bug preventing site admins to upload graphics in Admin Panel > Appearance > Customize > Graphics, in cases when site admins did not have user action ‘upload photos’;

Photos [photo]:
- added warning message when uploaded photo is bigger than the size defined in the plugin settings;
- fixed photo thumbs display for photo widget in mobile version;
- removed duplicate photos in the list of photos on the ‘Most discussed photos’ page;

Events [event]:
- fixed a bug allowing logged out users to edit events of other users;

Videos [video]:
- fixed the validation of video embed code during editing;

Friends [friends]:
- fixed a bug appearing when a user deletes someone from the friends list;

Newsfeed [newsfeed]:
- outbound links left by users are no longer converted to https, when SSL is active across the entire site;
- unless a user post features a thumbnail image, the post now fits the full width of the newsfeed;

Import Contacts [contact_importer]:
- added Send button when selecting Gmail contacts to invite;


Oxwall 1.8.1, Jan 12, 2016
====================================

Platform [core]:
- added mobile version for new Simplicity theme;
- license key is now required for commercial items during the installation of plugins/themes;
- list of photos available for avatar upload is no longer duplicated on the Change Avatar page;
- inverted commas within tags no longer cause errors on the content editing page;
- improved stability for captcha display;
- added new field type for fselect single choice, which allows to add unlimited number of values;
- added User's Timezone option to User Preferences;
- fixed Not Found errors for images on Admin Panel > Appearance > Customize > Graphics page;
- added basic customization option for mobile version theme in Admin Panel;
- improved Amazon S3 support;
- added option to disable captcha from Admin Panel;

Newsfeed [newsfeed]:
- private blog posts no longer show up in general Newsfeed;

Virtual Gifts [virtualgifts]:
- any selected gift is now shown as selected in Simplicity theme;

Forum [forum]:
- fixed link for creation of topics in Forum Topics index widget;
- added check during creation of new topic to see if a forum for this new topic exists;

Photos [photo]:
- empty albums no longer show up in User Albums widget on Profile View page;
- fixed photo search by tag bug;
- fixed bugs found during display of photos on photo lists;

Advertisement [ads]:
- fixed Google AdSense display bug;
- fixed conflict with Geolocation Data plugin;

TinyChat [tinychat]:
- added new user action "Use Chat";

Events [event]:
- only expired invitations are now deleted by cron;


Oxwall 1.8.0, Sep 8, 2015
====================================

Platform:
- introduced new default theme Simplicity (Frontend + Admin Panel);
- redesigned navigation and notification system in Admin Panel;
- added widget support in Admin Panel;
- reorganized pages/interfaces/controls in Admin Panel for improved simplicity and comprehension;
- fixed possible collision in database during user authorization;
- password for "Guests can view the site with password" mode is now encrypted;
- total interface overhaul for Admin panel >> Appearance >> Edit theme >> Graphics;
- fixed bug within mobile version preventing avatar attachment during registration;

Photos:
- fixed bug which duplicated photos in Top rated/Most discussed lists;
- empty albums are no longer displayed in album lists;
- added indices for fields entityId and entityType in table ow_photo_album;

Messages:
- fixed link display in new message notifications;
- fixed attachment display in mobile version;
- added chat/message link within new message notification template in mobile version;
- all latest messages are now viewable in mobile version;
- fixed search for messages;
- fixed message lists paging in mobile version;

Contact Importer:
- added support for latest Facebook API;

Facebook connect:
- added support for latest Facebook API;

Friends:
- enhanced synchronization with Newsfeed plugin;

Forum: 
- links within mobile version's notifications for new replies in subscribed topics now lead to mobile version's forum topic;


Oxwall 1.7.5, July 14, 2015
====================================

Platform:
- update server SSL connection fixed;
- floatbox language editing in the admin panel is now scrollable;
- links processing within content now recognizes periods and other full-stop symbols in sentences; 
- suspended users can now edit their avatars;
- mobile version: when users have no avatar selected, their Profile View page displays the default “No Avatar” image;
- generation of user hash salt passwords now employs the following method: UTIL_String::getRandomString
- if the service “add to friends” is not available, users can now delete other profiles from their friend lists;
- added mobile version of the WYSIWYG editor;
- fixed SMTP connection settings test in the admin panel;
- special symbols are no longer encoded in the Profile View page in the About Me widget; 

User Privacy:
- fixed the bug allowing one user accessing private photos of another user;

Messages:
- unused attachments are now deleted by cron;
- mobile version: fixed the markup for conversations/user list;

Newsfeed:
- unused attachments are now deleted from the file system;
- when user changes the avatar, it also updates in the 'birthday' item;

Forum:
- added mobile version;

Social Sharing:
- adapted for the site's mobile version;
- fixed the error 'Request-URI Too Large', which appeared when sharing content with extra volume of text/description;

Contacts Importer:
- Facebook API updated;
- added SSL support;


Oxwall 1.7.4, 2015-06-02
====================================

Platform:
- avatar size limit can be changed in admin area now
- fixed issues with responsive google ads displaying
- fixed issues with robots.txt syntax 
- Flag Content button shows only for loged in users now in mobile/desktop versions
- fixed issues with Custom Page termination
- fixed fatal error with Date field type on Search page
- added User list component

Forum:
- added advanced search
- added an optional search engine Zend Lucene - increases search results relevancy significantly 
- added "Filter by user" language key

Photos:
- now users can edit/view personal photos when service "View photo" is not active

Messages: 
- fixed issues with plugin using all memory running a cron task
- fixed issue with a Logged Out user showing as Online in Mobile Version
- fixed issue with Read messages showing as Unread
- fixed interface issues with Conversation Windows and Messages Page

Newsfeed:
- Like and Delete buttons work in mobile version now
- fixed issues with Status Update video upload
- fixed issue with an uploaded video not playing in mobile version

Groups: 
- added lang keys for group invitations in site console

Social Sharing:
- social services' management interface is based on Ajax now

Birthday:
- added missing lang keys
- fixed Birthday icon in Newsfeed item


Oxwall 1.7.3, 2015-04-14
====================================

Platform:
- dropped PHP 5.2 support;
- fixed issues with text editing in "Welcome Widget"
- fixed issues with saving settings in Admin Panel > Privacy&Permissions > Roles
- made custom "No avatar" image appear in all appropriate places on the site
- removed debug warning message on profile view page in the mobile version
- revised the apostrophe support for translations into other languages
- made language’s system prefixes importable
- removed the redundant setting "Allow photo upload" in Admin Panel > Settings > User Settings > Content Input
- fixed the display of a suspended user’s profile page in mobile version
- passwords set by the site admin under "Guests can view the site with password" mode are now encrypted
- fixed the bug preventing the user to proceed further from the Join page without uploading an avatar, under conditions of selected “display” option for “Display Photo Upload” setting
- fixed security issue related to ow_static folder

Newsfeed:
- fixed security issue allowing to delete other users’ comments

Messages:
- removed the ability to send empty messages
- fixed sound notifications
- fixed a JS error appearing when opening older messages during the message search of a specific user
- fixed the message display order in conversation during fast type
- activated the options button (gear) for conversations list in Chrome
- made the links inside conversations to display properly
- fixed the bug with perpetual preloader when user attempts to view conversation with no permissions
- fixed the link to a conversation posted within message text of email notifications concerning new messages

Geolocation data: 
- added new plugin

Photos:
- made it impossible to set "Maximum file size" bigger than "Server limit" in plugin settings
- fixed the display order of photos on the Photo List page in Firefox and IE
- made the “Add Photo” button disappear if the action is not available for a chosen user role

Forum: 
- fixed the error appearing during topic search by username

Contact importer:
- fixed fatal error appearing during user registration by invitation 


Oxwall 1.7.2, 2014-11-25
====================================

Platform:
- fully re-imagined and enhanced the “Flags” feature:
	- redesigned the page for moderators, to more effectively and simpler review and manage all flagged content. The link 	to the page will now appear in the Console for quicker access.
	- added the ability to flag all following content: users, events, comments, and newsfeed status updates.
- redesigned the interface for user avatar upload on "Join Form" and "Change Avatar" pages.
- added the option for admin/moderator to list the reason for the user suspension, which will be send to users’ email address.
- added the option for suspended users to delete their profiles from the site.
- fixed a bug affecting the user avatar display in console notifications after user changes avatars.
- the system now recognizes the value of php.ini directive “max_post_size” during the upload of a new theme archive.
- fixed a bug affecting the display of embed videos inserted through rich media in blogs, forum topics and newsfeed status updates.
- the invitation code is now removed from the database after the user is recognized as successfully registered on the site.
- made the invitations sent through Facebook contact importer eligible for registration, when “by invitations only” mode is on.
- added button "Mail notifications" in the Console for quicker access.
- during the import of language packs, only language keys of the installed plugins are added to the database now.
- removed the check for PHP directive "register_globals" in the installation script, since the directive is no longer supported by PHP http://php.net/manual/en/security.globals.php 
- fixed a bug which affected the behavior of frozen widgets in the Admin Area.
- fixed a bug which allowed a profile registered through Facebook Connect but without all required fields filled to appear on the site.
- made the label “More” in the context menu of the “View profile” page to be a part of the language system.
- added an error message to be displayed when a user changes password, but enters a wrong value during password confirmation.
- added correct https support for operation of individual SSL pages.
- introduced the size limit for the event log file. In addition, there is now an option to add exceptions to the log for the most frequent events.
- error log is now divided into separate contexts. 

Messages:
- the plugin’s performance and stability is significantly improved.
- increased the speed of search within conversations.
- increased the speed of user search during the creation of a new message.
- increased the display size of the conversation window.
- added formatting buttons, including bold, italic, underline, and link.
- added option to perform group actions with conversations.
- icons “envelope” and “bubble” are no longer displayed in the conversations list, if either of the Chat or Mailbox modes are on. 
- the behavior of the “Back” button for a conversation in the list is now more clear: it now appears only when a user added a conversation response. 
- added an attachment indicator for a conversation in the list, if it includes at least one attachment inside.
- the Console now loads more conversations during the first activation of the “Messages” button. 
- added plugin option “Allow to send messages once in…” for admin to prevent receiving spam sent by bots. 
- fixed the error “Call to a member function getId()”

Photos:
- fixed a bug preventing a photo to resize correctly during the switch from “View full size” to regular mode.
- fixed a bug affecting the display of photos in the album “Profile cover gallery”, when photos’ privacy is set to “My friends only”. 
- fixed the display of the photo description in the “Photo view” page title.view
- added social sharing buttons on the “Photo view” page, if the Social Sharing plugin is installed.
- added option to include hashtags for photos in any language. 
- fixed a bug preventing the editing of album covers if the Amazon Cloud mode is activated on the site. 
- fixed the display of the meta tag value “description” on the page “Most discussed photos”
- reduced space size taken by photos after conversion. The reduction is achieved through lowering of the end quality ration during the conversion. 

Blogs:
- “Edit” button is no longer displayed to moderators, unless they are specifically assigned blog moderation rights.
- fixed the display format of a newsfeed record about the creation of new blog posts. 

Video:
- added support of thumbnail grabbing for embed videos from Facebook. 
- fixed the display of embed videos, which had percentage values for width in their embed code.

Newsfeed:
- fixed a bug allowing a user to delete another user’s post after leaving a comment after it.

Contact us:
- captcha field is now displayed on Contact form for suspended users.


Oxwall 1.7.1, 2014-08-25:
====================================

Platform:
- added join form for mobile version
- reorganized action buttons for profiles on the profile view page; added buttons 'more' and 'moderate' for grouping actions
- fixed default avatar image vulnerability in the Admin Panel
- fixed the bug preventing the save of changes in the admin panel > user settings >general due to the error 'The image is not valid'
- introduced truncation for all comments, together with a button 'View more' for comments longer than 150 symbols
- fixed the display of action buttons for profiles in mobile version
- added option to create links to external sites in mobile menu
- introduced design improvements within interfaces used for working with account types
- made the embedded videos playable on site, without the need to leave for external destinations

Messages:
- added form for creating new messages with selection of a recipient
- added batch of performance improvements
- added a tooltip with user info for user avatars' mouse-overs
- added invitation labels within text inputs for better clarity
- added option to send messages to users who are not allowed to access 'read', 'write' and 'continue chat' services, in cases when the site features pre-installed plugins Memberships and User Credits
- made the button 'Chat now' disappear when user is online and the mode 'Chat Only' is turned on
- added new line formatting fix

Photos:
- made the software recognize both PHP settings - "post_max_size" and "upload_max_filesize" - during the calculation of a file's maximum limit for upload
- made the action buttons for albums appear on the 'view album' page
- optimized the display performance of 'User's albums' widget on the profile view for users with a large number of photos
- fixed the bug affecting 'Add photo' button for users with unavailable 'upload photos' service

Groups:
- made the group description text cut-off after 300 symbols on the group listing page
- made the user automatically unfollow the group after leaving it
- fixed bug allowing unlogged users to delete wall comments

Forum:
- added performance optimization for supporting large number of topics

Video:
- fixed vimeo support

Birthdate:
- added batch of design improvements for the widget and newsfeed listing

Events:
- fixed display of private events in user dashboard


Oxwall 1.7.0, 2014-07-08:
====================================

Platform:
- reduced base.css file size by moving admin panel css to separate file /admin/css/admin.css
- redesigned installation process
- updated Amazon S3 libraries
- updated PHPMailer library
- added optional error log file
- redesigned files/photos/videos attachments used by comments, messages, forum, etc.
- fixed attachments in mobile version on Amazon S3 to make them storable
- updated user input filtering settings to prevent XSS and invalid html content
- fixed join form to prevent it from resetting without a user joining
- fixed the issue with failure to send notifications if a user hasn't changed notifications preferences
- updated system 500 error page with error details for admin (!)
- added option to update plugins by uploading them from admin panel via "add new" plugin form
- fixed error appearing when a new plugin is added with duplicate folder name
- dropped IE9 support
- added IE11 support
- extended the list of errors with FTP operations
- improved account types support
- added option to assign specific user roles for each account type
- added option to assign separate list of profile questions for each account type
- fixed the desktop version link in the mobile version for cases when content is not available in the mobile version
- redesigned comment box
- added proper user login redirect, sending users to the first page in the main menu, accessible only to logged-in users
- fixed displaying columns for "single choice" profile questions on search form
- fixed unsubscribe from site notifications option
- added option to remove site theme from admin panel
- made automatic removal of outgoing mails from ow_base_mail table if a user was deleted from the site
- added option to disable site mobile version from the admin panel
- made values removal automatically if a related question was deleted
- fixed WYSIWYG editor in IE11
- replaced WURFL library with Mobileesp
- fixed invalid routing when site is installed into subfolder with "www" as part of domain name
- fixed user redirect from mobile to desktop version for non-logged-in users with "guests can view the site" option disabled

Virtual gifts:
- fixed category display on the page ‘Add new gift’

 Facebook connect:
- added additional step with required profile questions after the first sign-up

Events:
- made invitations removal for passed events automatically
- applied user permission "view event" to event lists
- fixed displaying updated event title in newsfeed

Mailbox->Messages:
- complete redesign and merger with Instant Chat, becoming a new single plugin called Messages
- added mobile version support
- added indication for sender if a recipient profile is suspended

Newsfeed:
- redesigned photos displaying format
- added option to remove comments from other users on profile page for profile owner
- fixed items sorting on my profile's newsfeed

Videos:
- updated embed code filtering to prevent non valid html
- made all embed videos posted through newsfeed status update automatically saved to the profile’s videos

Photos:
- redesigned plugin
    - new upload process
    - 2 modes of photo view (vertical, horizontal)
    - 2 modes of photo list (classic, pinterest)
    - search photos by username, hashtags
    - tons of other improvements
- added option to download photos for site users
- fixed photos’ links in notification in mobile version
- made all photos posted through newsfeed status update automatically saved to the user's album
- optimized photo processing to reduce disk space usage

Friends:
- removed moderation option from admin panel
- fixed user follow logic: user A starts following user B’s content if user B accepts a friend request
- fixed warning message when friends plugin is deactivated

Groups:
- fixed displaying updated group title on the new group forum creation page, if the title has been changed previously
- added an ability to customize group's page for site moderator

Forum:
- fixed search option in IE10/IE11

Blogs:
- fixed center align option on add new image page

Birthdays:
- fixed "view all" link on index widget


Oxwall 1.6.0, 2014-01-08:
====================================

Platform:
- added mobile version platform, supporting following features: 
    - navigation
    - system pages (splash screen, site maintenance, user not reviewed, passworded site access, etc.)
    - user profile (sign-in, view, list)
    - photos (upload, view)
    - newsfeed (base, photos)
    - real time activity notifications (base, comments, friends, groups, events)
    - moderation options (profile deletion, suspension)
    - mobile theme customization
    - facebook connect
    - reset password
    - RTL support
    - auto-login for returning visitors
- updated jquery library to version 2.0.3
- added PHP 5 support
- added theme autoupdate support
- fixed issue with sent letters not being deleted from the database during cron execution
- added site user status recognition (not approved, suspended, etc.) when they are displayed in site listings
- removed duplicated indexes in core database
- fixed issue with non-recognition of changes made to the profile questions on the join form
- removed duplicate meta tags, and added new meta tags to plugin and core pages
- added proper support of remote user IP when the software operates via Nginx and/or Cloudflare
- removed option "Column count" for profile questions, which lack multiple choice values
- fixed regexp validation for form fields like email
- fixed issue with profile registration when the site features several account types and is closed for password access
- made join form to check username for uniqueness when site access is closed for not logged-in users
- fixed issue with inability to add new menu items in the main section when it is empty
- fixed issue with failure to display video thumbnails for YouTube videos uploaded through media panel
- added check for removal of install folder after successful software installation (for security reasons)
- fixed issue with failure to add lang key, when default language is not active
- added check for module name when adding new plugin through admin area
- introduced ajax for button actions on profile view: suspend, make featured/remove from featured, block/unblock
- removed option to deactivate default language if no other languages are present on site
- fixed paging on page with user list
- fixed issue with failure to send users mail notifying them of profile approval, when approval is done from view profile page

Themes:
- new theme ‘Munchen’

Social Sharing:
- added new plugin to allow users share site content on popular social networks

Newsfeed:
- defined output formats
- fixed issue allowing one user to delete another user’s comment after liking it in newsfeed 
- fixed issue allowing blocked user to leave comments on the profile which initiated the block
- fixed issue with displaying thumbnails for YouTube videos
- added support for non-standard ports
- fixed issue with inability to delete added video in status update

Forum:
- added option to search topic by username
- made forum index display forum topic list if forum contains only one section with a single sub-forum
- added separate page for forum section

Blogs:
- fixed posts sorting in archive and during tag search
- fixed fatal error on page displaying all posts of a specific user
- fixed issue allowing any user to edit any post by accessing it through direct URL
- fixed issue with displaying big photos in posts

Events:
- added lang keys for accept and ignore buttons
- fixed issue with failure to delete newsfeed entries for events removed from site
- fixed typos in code
- fixed issue with javascript processing non-latin symbols

Groups:
- fixed issue allowing any user to join private groups through direct URL 
- fixed issue with javascript processing non-latin symbols
- fixed issue with failure to unsubscribe users from group newsfeed updates after leaving the group

Photos:
- added special hash to photo file names for improved security. (Fix is applied only to new photos).

Videos:
- added video thumbnail caching for improved site performance


Oxwall 1.5.3, 2013-04-16:
==============================

Platform:
- fixed the cron job notification in admin area even a cron command is setup right


Oxwall 1.5.2, 2013-04-08:
==============================

Platform:
- run the cron job on page refresh
- redesigned tag input
- Direct view permissions management for index/dashboard/my profile widgets.
- fixed minor issues with the default Origin theme
- fixed glitch with single choice/drop down profile questions
- installation script now overwrites config.php if permissions are allowed
- fixed markup issue on Privacy&Permissions page in admin area
- fixed markup issue on Pages&Menus page when too many menu items are added to the main menu area
- rss widget: links now open in new window
- added default delimiters in toolbar for IPC decorator
- redesigned "Choose theme" page in admin area
- fixed an ability to remove account type if any profile questions are assigned to it
- fixed a glitch with too long titles for widgets on site index/dashboard/profile view pages

Themes:
- new ShowCase

Activity Notifications:
- added an option for users to receive notifications immediately
- added notification when someone posts a status on user's profile page

Import contacts:
- added invitation by email
- fixed facebook invitation page
- added HTTPS support for facebook import configuration ( Secure Canvas URL)

Mailbox:
- fixed markup issues

Blogs:
- add My Drafts button

Cloudflare:
- added new plugin to support CloudFlare service

Photos:
- added "Upload photos" button on "view photo album" page
- redesigned comment box
- redesigned "Add photo" page

Events:
- redesigned attendance buttons

Newsfeed:
- fixed a link to profile in birthdate entry

Forum:
- changed the way attachments are named


Oxwall 1.5.0, 2012-12-19:
==============================

Platform:
- New real-time notification system
- Redesigned user console
- The new default theme: Origin
- Added ability for moderators to modify users' profile info and view hidden fields
- Improved widget panels performance
- Profile view buttons now handled with ajax
- RSS atom support for RSS widgets
- Template files can no longer use PHP inside smarty code
- Optimized user lists management in the admin panel
- Some friend-only content is now properly shown to friends
- Cloud files mime type processing
- Photo upload requirement on the registration form can now be removed
- The ability to flag user's own content
- Display paging navigation when browsing content by tags
- Proper headers for "404 not found" page
- Double slashes issue in custom page URL
- Profile questions labels
- URLs for flagged photos in the moderation panel
- "Follow" button now properly changes to "unfollow" after page reload
- Resolved multiple issues with language management in the admin panel
- User roles order in role management interface now defines avatar badge display
- URL validation for custom pages
- Fixed security issue into widget panel
- Fixed issue with admin’s ability of deleting himself via Newsfeed comments;
- Removed button allowing admin delete his profile via profile page;
- Fixed issue with not working context actions after comment deletion;

Watchdog:
- The new antispam plugin

Video:
- Thumbnails for Vimeo, xhamster.com now get cropped again
- Rate system improved by also counting the number of votes
- Performance optimization

Instant Chat:
- Completely redesigned
- time of the last messages is now correct
- Fixed displaying the number of online users above 14
- Fixed fake bruteforce alert when a few chat windows are opened
- Added a preloader that disappears once online users list is loaded;
- Performance optimization

Blogs:
- New interface for draft posts view
- Fixed after-draft post date
- Rate system improved by also counting the number of votes
- Fixed sort order for updated posts
- Fixed drag'n'drop error in IE8

Photos:
- Fixed unclickable "Add new" link in the photo widget
- Fixed the permission bug for private photos
- Rate system improved by also counting the number of votes
- Removed comment option for the list of photos in the newsfeed
- Updated Flash Photo Uploader;
- Performance optimization

Forum:
- At topic creation, "subscribe to this topic" option now checked by default

Groups:
- Ability to remove members from group
- Permission check for group view on the group list and the groups widget

Newsfeed:
- Performance improvement: old unused items removal + content caching
- Added an ability of ‘liking’ your own Newsfeed items;

Events:
- Permission check for event view in the events widget
- Suspended users no longer displayed on the participants' list

Facebook Connect:
- Facebook Connect Synchronization improvements and minor fixes


Oxwall 1.4.1, 2012-10-09:
============================
Platform:
 - user role management security fix;
 - prevention of possible XSS attacks in profile questions;

Oxwall 1.4, 2012-06-21:
============================

Platform:
- new dashboard widget "Quick links", instead of separate plugin widgets;
- comments: ability to choose preview images for posted URLs;
- new design element, Context Action: currently on photo view only.
- moderators now can see private content for moderation;
- form buttons location redesign;
- various language strings fixed;
- flagging now works without page reload;
- fixed online user display in case of "me only" mode;
- widget panel was optimized for better performance;
- floatbox refactored;

Photos:
- redesigned photo browsing;
- private photos: fixed display in top rated list;
- fixed bug when photos are uploaded under HTTPS;

Import Contacts:
- Google contact import is back and improved;

Forum:
- forum: added search results order by date and relevance;
- fixed an error with too long topic text;

Birthdate:
- birthdate fields (date/month/day) can be translated via Language section;

Video:
- video: long titles and descriptions are now truncated;

Newsfeed:
- profile newsfeed: new ability for others to post;
- main site newsfeed enhanced;

Groups:
- group list: fixed double paging;


Oxwall 1.3.2, 2012-03-21:
==============================

Platform:
- Cron setup changed (now uses HTTP);
- Default user role is now impossible to remove;
- Fixed the bug with the number of pics for WYSIWYG gallery;
- Notifications "Someone posts a wall comment in a group I participate in",     "Someone invites me to a group", etc., enabled by default;
- Additional admin now can't delete the super admin profile;
- XSS vulnerability in the update script fixed;
- Added file_get_contents check on server;
- While editing a custom page it's no longer possible to enter existing pages' URLs.
- Added rel="nofollow" for auto-linking and WYSIWYG;
- Changed buttons for group actions on profile lists in admin area;
- Removed Exception message that happened while approving an already approved member;
- Changed the order of displaying CSS graphics in the admin area;
- Multiple language entries corrected.

Blogs:
- Post tags are now added to meta keywords;
- Added messages about successful post creation and editing;

Friends:
- Fixed friend request template;
- With friend request a user automatically follows another user;

Instant Chat:
- Fixed 'OW Debug' error message when admins deactivated 'Friends' plugin;
- Fixed 'last activity 42 years ago' bug;
- Removed switching ‘for all’ and ‘friends only’ modes, making it dependent on the 'Friends' plugin;

Links:
- 'More' button does not stick to the last letter any more;
- Links now open in the new window;

Forum:
- 'Ghost' topics now removed in five days after the original topic move;
- User no longer redirected to a new forum section after moving a topic;
- Fixed 'Latest Reply' field when author profile deleted;

Video:
- Fixed Flash object overlap;

Advertisement:
- Now more than 14 banners can be added to one ad place;
- Added the 'Hide Ads' authorization action for user roles;

Events:
- New events are now at the top of the list;
- Long event locations now stay within widget;
- If 'Friends' plugin deactivated you can invite all site users (who were not invited yet and are not registered for event);
- Invite interface now shows all site users (up to 100) if 'Friends' plugin is inactive;
- Added 'Accept/Decline' buttons to event invitations;
- Event notification now disappears after visiting event page;

Mailbox:
- Fixed avatar while sending private messages from profile;

Privacy:
- If 'Friends' plugin deactivated all ‘Friends Only’ settings change to ‘Only Me’;

Groups:
- If 'Friends' plugin deactivated you can now invite all site users (up to 100);
- Group listings changed;
- Invite notifications now disappear after visiting invitation list or group pages;

Newsfeed:
- Redesigned group activity display;
- Individual pages for every newsfeed item;
- New option to choose preview picture for attached URLs;

Birthdays:
- E-mail notifications about new comments or likes for birthday items;


Oxwall 1.3.0, 2012-02-07:
=========================

Platform
- Added Smarty 3 support;
- Redesigned Developer Tools widget;
- Disabled WYSIWYG for mobile devices;
- Fixed XSS in file comment's attachments;
- Added group action to "Unverify Email" for user lists in admin panel;
- Added support of synchronization between different products of the same payment system;
- Added selection of user roles for mass mailing;
- Fixed: welcome letter is sent only after email address verification;
- Fixed scrolling in floatbox;
- Truncated Javascript in widget titles;
- Added "Block User" feature;

Plugins
- Forum: added warning message if not all attachments were uploaded;
- Forum: added "Private Forum" option;
- Forum: fixed access to group's forum;
- Events: changed presentation of "Start Date" and "End Date" fields;
- Events: fixed private events displayed on public listings;
- Newsfeed: fixed interaction with private items such as groups, private events;
- Private groups: new plugin;
- Import Contacts: new plugin;
- Blogs: truncated blog's description in widgets;
- Links: truncated links's description in widgets;
