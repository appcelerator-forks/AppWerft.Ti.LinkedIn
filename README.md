Ti.LinkedIn
===========

This is a module for getting some infos from LinkedInportal. With it you can aslo share to profile.
Oauth2.0 is included. You need appId and appSecret. Both must be added to tiapp.xml as String property

Usage
-----

It is a very simple API:

~~~

var LinkedIn = require('de.appwerft.linkedin');
LinkedIn.getProfile('me', function(_e) {
    alert(_e.data);
});
~~~

More getter are: getPositionById(), getCompanyById, postShare(), getProfileWithContacts();

For all request you need scopes (see documentation). As allowed redirect_uri you must add  'https://upload.wikimedia.org/wikipedia/en/b/b1/Portrait_placeholder.png'. This is dirty workeround, because LinkedIn doesn't support oob.

These are entry in you tiapp.xml:

~~~
<property name="linkedin_id" type="string">7798****xfs</property>
<property name="linkedin_secret" type="string">wqApS***54G8Ky</property>

/* optional*/
<property name="linkedin_redirecturl" type="string">https://upload.wikimedia.org/wikipedia/en/b/b1/Portrait_placeholder.png</property>

~~~

![]()