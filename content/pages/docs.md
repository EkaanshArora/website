Title: API Documentation
Slug: docs
Summary: The SpaceAPI format documentation.

It's highly recommended to use the explicit specified fields from the
reference. If you need other fields additionally, please make a change request.
Or prefix custom fields with `ext_` to make it clear the field is not part of
the documented API. Consumers are not obligated to interpret any custom fields.

Most types are not nullable. That means that they may not contain the value "null",
but they may be left away if they're not required.

<ul class="group apidocs">
<li><section class="item">
<header>
<h3>api</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The version of SpaceAPI your endpoint uses</p>
<h4>Valid values</h4>
<p><code>0.13</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>space</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The name of your space</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>logo</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>URL to your space logo</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>url</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>URL to your space website</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Position data such as a postal address or geographic coordinates</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>address</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The postal address of your space (street, block, housenumber, zip code, city, whatever you usually need in your country, and the country itself).<br>Examples: <ul><li>Netzladen e.V., Breite Straße 74, 53111 Bonn, Germany</li></ul></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>lat</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Latitude of your space location, in degree with decimal places. Use positive values for locations north of the equator, negative values for locations south of equator.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>lon</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Longitude of your space location, in degree with decimal places. Use positive values for locations west of Greenwich, and negative values for locations east of Greenwich.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>spacefed</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A flag indicating if the hackerspace uses SpaceFED, a federated login scheme so that visiting hackers can use the space WiFi with their home space credentials.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>spacenet</h3><span class="type">(boolean)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>See the <a target="_blank" href="https://spacefed.net/wiki/index.php/Category:Howto/Spacenet">wiki</a>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>spacesaml</h3><span class="type">(boolean)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>See the <a target="_blank" href="https://spacefed.net/wiki/index.php/Category:Howto/Spacesaml">wiki</a>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>spacephone</h3><span class="type">(boolean)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>See the <a target="_blank" href="https://spacefed.net/wiki/index.php/Category:Howto/Spacephone">wiki</a>.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>cam</h3><span class="type">(array of string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>URL(s) of webcams in your space</p>
<h4>Minimum number of items</h4>
<p>1</p>
<h4>Nested array items</h4>
<span>string</span>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>stream</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A mapping of stream types to stream URLs.If you use other stream types make a <a href="add-your-space" target="_blank">change request</a> or prefix yours with <samp>ext_</samp> .</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>m4</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Your mpg stream URL. Example: <samp>{"mp4": "http//example.org/stream.mpg"}</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>mjpeg</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Your mjpeg stream URL. Example: <samp>{"mjpeg": "http://example.org/stream.mjpeg"}</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>ustream</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Your ustream stream URL. Example: <samp>{"ustream": "http://www.ustream.tv/channel/hackspsps"}</samp></p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>state</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A collection of status-related data: actual open/closed status, icons, last change timestamp etc.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>open</h3><span class="type">(boolean)</span>
<span class="tag required">required</span>
<span class="tag nullable">nullable</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A flag which indicates if the space is currently open or closed. The state 'undefined' can be achieved by assigning this field the value 'null' (without the quotes). In most (all?) programming languages this is evaluated to false so that no app should break</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>lastchange</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The Unix timestamp when the space status changed most recently</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>trigger_person</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The person who lastly changed the state e.g. opened or closed the space.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>message</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An additional free-form string, could be something like <samp>'open for public'</samp>, <samp>'members only'</samp> or whatever you want it to be</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>icon</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Icons that show the status graphically</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>open</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The URL to your customized space logo showing an open space</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>closed</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The URL to your customized space logo showing a closed space</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>events</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Events which happened recently in your space and which could be interesting to the public, like 'User X has entered/triggered/did something at timestamp Z'</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Name or other identity of the subject (e.g. <samp>J. Random Hacker</samp>, <samp>fridge</samp>, <samp>3D printer</samp>, …)</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Action (e.g. <samp>check-in</samp>, <samp>check-out</samp>, <samp>finish-print</samp>, …). Define your own actions and use them consistently, canonical actions are not (yet) specified</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>timestamp</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Unix timestamp when the event occured</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>extra</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A custom text field to give more information about the event</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>contact</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Contact information about your space. You must define at least one which is in the list of allowed values of the issue_report_channels field.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>phone</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Phone number, including country code with a leading plus sign. Example: <samp>+1 800 555 4567</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>sip</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>URI for Voice-over-IP via SIP. Example: <samp>sip:yourspace@sip.example.org</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>keymasters</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Persons who carry a key and are able to open the space upon request. One of the fields irc_nick, phone, email or twitter must be specified.</p>
<h4>Minimum number of items</h4>
<p>1</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Real name</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>irc_nick</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Contact the person with this nickname directly in irc if available. The irc channel to be used is defined in the contact/irc field.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>phone</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Example: <samp>['+1 800 555 4567','+1 800 555 4544']</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>email</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Email address which can be base64 encoded.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>twitter</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Twitter username with leading <samp>@</samp>.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>irc</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>URL of the IRC channel, in the form <samp>irc://example.org/#channelname</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>twitter</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Twitter handle, with leading @</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>facebook</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Facebook account URL.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>google</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Google services.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>plus</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Google plus URL.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>identica</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Identi.ca or StatusNet account, in the form <samp>yourspace@example.org</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>foursquare</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Foursquare ID, in the form <samp>4d8a9114d85f3704eab301dc</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>email</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>E-mail address for contacting your space. If this is a mailing list consider to use the contact/ml field.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>ml</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The e-mail address of your mailing list. If you use Google Groups then the e-mail looks like <samp>your-group@googlegroups.com</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>jabber</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A public Jabber/XMPP multi-user chatroom in the form <samp>chatroom@conference.example.net</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>issue_mail</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A seperate email address for issue reports (see the <em>issue_report_channels</em> field). This value can be Base64-encoded.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>issue_report_channels</h3><span class="type">(array of string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This array defines all communication channels where you want to get automated issue reports about your SpaceAPI endpoint from the revalidator. This field is meant for internal usage only and it should never be consumed by any app. At least one channel must be defined. Please consider that when using <samp>ml</samp> the mailing list moderator has to moderate incoming emails or add the sender email to the subscribers. If you don't break your SpaceAPI implementation you won't get any notifications ;-)</p>
<h4>Minimum number of items</h4>
<p>1</p>
<h4>Nested array items</h4>
<span>string</span>
<h5>Valid values</h5>
<p><code>email</code> | <code>issue_mail</code> | <code>twitter</code> | <code>ml</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>sensors</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Data of various sensors in your space (e.g. temperature, humidity, amount of Club-Mate left, …). The only canonical property is the <em>temp</em> property, additional sensor types may be defined by you. In this case, you are requested to share your definition for inclusion in this specification.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>temperature</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Temperature sensor. To convert from one unit of temperature to another consider <a href="http://en.wikipedia.org/wiki/Temperature_conversion_formulas" target="_blank">Wikipedia</a>.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value.</p>
<h4>Valid values</h4>
<p><code>°C</code> | <code>°F</code> | <code>K</code> | <code>°De</code> | <code>°N</code> | <code>°R</code> | <code>°Ré</code> | <code>°Rø</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>door_locked</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Sensor type to indicate if a certain door is locked.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(boolean)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>front door</samp>, <samp>chill room</samp> or <samp>lab</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>barometer</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Barometer sensor</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>hPA</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>radiation</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Compound radiation sensor. Check this <a rel="nofollow" href="https://sites.google.com/site/diygeigercounter/gm-tubes-supported" target="_blank">resource</a>.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>alpha</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An alpha sensor</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Observed counts per minute (ocpm) or actual radiation value. If the value are the observed counts then the dead_time and conversion_factor fields must be defined as well. CPM formula: <div>cpm = ocpm ( 1 + 1 / (1 - ocpm x dead_time) )</div> Conversion formula: <div>µSv/h = cpm x conversion_factor</div></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Choose the appropriate unit for your radiation sensor instance.</p>
<h4>Valid values</h4>
<p><code>cpm</code> | <code>r/h</code> | <code>µSv/h</code> | <code>mSv/a</code> | <code>µSv/a</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>dead_time</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The dead time in µs. See the description of the value field to see how to use the dead time.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>conversion_factor</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The conversion from the <em>cpm</em> unit to another unit hardly depends on your tube type. See the description of the value field to see how to use the conversion factor. <strong>Note:</strong> only trust your manufacturer if it comes to the actual factor value. The internet seems <a rel="nofollow" href="http://sapporohibaku.wordpress.com/2011/10/15/conversion-factor/" target="_blank">full of wrong copy & pastes</a>, don't even trust your neighbour hackerspace. If in doubt ask the tube manufacturer.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>beta</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A beta sensor</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Observed counts per minute (ocpm) or actual radiation value. If the value are the observed counts then the dead_time and conversion_factor fields must be defined as well. CPM formula: <div>cpm = ocpm ( 1 + 1 / (1 - ocpm x dead_time) )</div> Conversion formula: <div>µSv/h = cpm x conversion_factor</div></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Choose the appropriate unit for your radiation sensor instance.</p>
<h4>Valid values</h4>
<p><code>cpm</code> | <code>r/h</code> | <code>µSv/h</code> | <code>mSv/a</code> | <code>µSv/a</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>dead_time</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The dead time in µs. See the description of the value field to see how to use the dead time.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>conversion_factor</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The conversion from the <em>cpm</em> unit to another unit hardly depends on your tube type. See the description of the value field to see how to use the conversion factor. <strong>Note:</strong> only trust your manufacturer if it comes to the actual factor value. The internet seems <a rel="nofollow" href="http://sapporohibaku.wordpress.com/2011/10/15/conversion-factor/" target="_blank">full of wrong copy & pastes</a>, don't even trust your neighbour hackerspace. If in doubt ask the tube manufacturer.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>gamma</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A gamma sensor</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Observed counts per minute (ocpm) or actual radiation value. If the value are the observed counts then the dead_time and conversion_factor fields must be defined as well. CPM formula: <div>cpm = ocpm ( 1 + 1 / (1 - ocpm x dead_time) )</div> Conversion formula: <div>µSv/h = cpm x conversion_factor</div></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Choose the appropriate unit for your radiation sensor instance.</p>
<h4>Valid values</h4>
<p><code>cpm</code> | <code>r/h</code> | <code>µSv/h</code> | <code>mSv/a</code> | <code>µSv/a</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>dead_time</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The dead time in µs. See the description of the value field to see how to use the dead time.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>conversion_factor</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The conversion from the <em>cpm</em> unit to another unit hardly depends on your tube type. See the description of the value field to see how to use the conversion factor. <strong>Note:</strong> only trust your manufacturer if it comes to the actual factor value. The internet seems <a rel="nofollow" href="http://sapporohibaku.wordpress.com/2011/10/15/conversion-factor/" target="_blank">full of wrong copy & pastes</a>, don't even trust your neighbour hackerspace. If in doubt ask the tube manufacturer.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>beta_gamma</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A sensor which cannot filter beta and gamma radiation seperately.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Observed counts per minute (ocpm) or actual radiation value. If the value are the observed counts then the dead_time and conversion_factor fields must be defined as well. CPM formula: <div>cpm = ocpm ( 1 + 1 / (1 - ocpm x dead_time) )</div> Conversion formula: <div>µSv/h = cpm x conversion_factor</div></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Choose the appropriate unit for your radiation sensor instance.</p>
<h4>Valid values</h4>
<p><code>cpm</code> | <code>r/h</code> | <code>µSv/h</code> | <code>mSv/a</code> | <code>µSv/a</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>dead_time</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The dead time in µs. See the description of the value field to see how to use the dead time.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>conversion_factor</h3><span class="type">(number)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The conversion from the <em>cpm</em> unit to another unit hardly depends on your tube type. See the description of the value field to see how to use the conversion factor. <strong>Note:</strong> only trust your manufacturer if it comes to the actual factor value. The internet seems <a rel="nofollow" href="http://sapporohibaku.wordpress.com/2011/10/15/conversion-factor/" target="_blank">full of wrong copy & pastes</a>, don't even trust your neighbour hackerspace. If in doubt ask the tube manufacturer.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>humidity</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Humidity sensor</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>%</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>beverage_supply</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>How much Mate and beer is in your fridge?</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit, either <samp>btl</samp> for bottles or <samp>crt</samp> for crates.</p>
<h4>Valid values</h4>
<p><code>btl</code> | <code>crt</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Room 1</samp> or <samp>Room 2</samp> or <samp>Room 3</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>power_consumption</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The power consumption of a specific device or of your whole space.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>mW</code> | <code>W</code> | <code>VA</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>wind</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Your wind sensor.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>properties</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>speed</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>m/s</code> | <code>km/h</code> | <code>kn</code></p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>gust</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>m/s</code> | <code>km/h</code> | <code>kn</code></p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>direction</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The wind direction in degrees. Use this <a href="https://github.com/slopjong/OpenSpaceLint/issues/80" target="_blank_">mapping</a> to convert the degrees into a string.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>°</code></p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>elevation</h3><span class="type">(object)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Height above mean sea level.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The sensor value</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The unit of the sensor value. You should always define the unit though if the sensor is a flag of a boolean type then you can of course omit it.</p>
<h4>Valid values</h4>
<p><code>m</code></p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>network_connections</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This sensor type is to specify the currently active  ethernet or wireless network devices. You can create different instances for each network type.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is optional but you can use it to the network type such as <samp>wifi</samp> or <samp>cable</samp>. You can even expose the number of <a href="https://spacefed.net/wiki/index.php/Spacenet" target="_blank">spacenet</a>-authenticated connections.</p>
<h4>Valid values</h4>
<p><code>wifi</code> | <code>cable</code> | <code>spacenet</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The amount of network connections.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>machines</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The machines that are currently connected with the network.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The machine name.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>mac</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The machine's MAC address of the format <samp>D3:3A:DB:EE:FF:00</samp>.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The location of your sensor such as <samp>Outside</samp>, <samp>Inside</samp>, <samp>Ceiling</samp>, <samp>Roof</samp> or <samp>Room 1</samp>.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>This field is an additional field to give your sensor a name. This can be useful if you have multiple sensors in the same location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>account_balance</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>How rich is your hackerspace?</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>How much?</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>unit</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>What's the currency? If your currency is missing open a new <a href="https://github.com/slopjong/OpenSpaceLint/issues" target="_blank">issue</a> and request the addition of your currency according <a href="http://de.wikipedia.org/wiki/ISO_4217" target="_blank">ISO 4217</a>.</p>
<h4>Valid values</h4>
<p><code>BTC</code> | <code>EUR</code> | <code>USD</code> | <code>GBP</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>If you have more than one account you can use this field to specify where it is.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Give your sensor instance a name.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>total_member_count</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Specify the number of space members.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The amount of your space members.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Specify the location if your hackerspace has different departments (for whatever reason). This field is for one department. Every department should have its own sensor instance.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>You can use this field to specify if this sensor instance counts active or inactive members.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>people_now_present</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Specify the number of people that are currently in your space. Optionally you can define a list of names.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>value</h3><span class="type">(number)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The amount of present people.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>location</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>If you use multiple sensor instances for different rooms, use this field to indicate the location.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Give this sensor a name if necessary at all. Use the location field for the rooms. This field is not intended to be used for names of hackerspace members. Use the field 'names' instead.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>names</h3><span class="type">(array of string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>List of hackerspace members that are currently occupying the space.</p>
<h4>Minimum number of items</h4>
<p>1</p>
<h4>Nested array items</h4>
<span>string</span>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>description</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>An extra field that you can use to attach some additional information to this sensor instance.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>feeds</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Feeds where users can get updates of your space</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>blog</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Type of the feed, for example <samp>rss</samp>, <samp>atom</atom>, <samp>ical</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>url</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Feed URL</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>wiki</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Type of the feed, for example <samp>rss</samp>, <samp>atom</atom>, <samp>ical</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>url</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Feed URL</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>calendar</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Type of the feed, for example <samp>rss</samp>, <samp>atom</atom>, <samp>ical</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>url</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Feed URL</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>flickr</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p></p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Type of the feed, for example <samp>rss</samp>, <samp>atom</atom>, <samp>ical</samp></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>url</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Feed URL</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>cache</h3><span class="type">(object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Specifies options about caching of your SpaceAPI endpoint. Use this if you want to avoid hundreds/thousands of application instances crawling your status.</p>
<h4>Nested object properties</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>schedule</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Cache update cycle. This field must match the basic regular expression <code>^[mhd]\.[0-9]{2}$</code>, where the first field specifies a unit of time (<code>m</code> for 1 minute, <code>h</code> for 1 hour, <code>d</code> for 1 day), and the second field specifies how many of this unit should be skipped between updates. For example, <samp>m.10</samp> means one updates every 10 minutes, <samp>h.03</samp> means one update every 3 hours, and <samp>d.01</samp> means one update every day.</p>
<h4>Valid values</h4>
<p><code>m.02</code> | <code>m.05</code> | <code>m.10</code> | <code>m.15</code> | <code>m.30</code> | <code>h.01</code> | <code>h.02</code> | <code>h.04</code> | <code>h.08</code> | <code>h.12</code> | <code>d.01</code></p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>projects</h3><span class="type">(array of string)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Your project sites (links to GitHub, wikis or wherever your projects are hosted)</p>
<h4>Nested array items</h4>
<span>string</span>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>radio_show</h3><span class="type">(array of object)</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>A list of radio shows that your hackerspace might broadcast.</p>
<h4>Nested array items</h4>
<ul class="group">
<li><section class="item">
<header>
<h3>name</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The name of the radio show.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>url</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The stream URL which must end in a filename or a semicolon such as <br><ul><li>http://signal.hackerspaces.org:8090/signal.mp3</li><li>http://85.214.64.213:8060/;</ul></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>type</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>The stream encoder.</p>
<h4>Valid values</h4>
<p><code>mp3</code> | <code>ogg</code></p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>start</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Specify the start time by using the <a href="http://en.wikipedia.org/wiki/ISO_8601" target="_blank">ISO 8601</a> standard. This encodes the time as follows: <br><br><ul><li>Combined date and time in UTC: 2013-06-10T10:00Z</li><li>Combined date and time in localtime with the timezone offset: 2013-06-10T12:00+02:00</li><li>Combined date and time in localtime with the timezone offset: 2013-06-10T07:00-03:00</li></ul> The examples refer all to the same time.</p>
<div></details>
</section></li>
<li><section class="item">
<header>
<h3>end</h3><span class="type">(string)</span>
<span class="tag required">required</span>
</header>
<details class="togglable">
<summary>Details</summary>
<div>
<p>Specify the end time by using the <a href="http://en.wikipedia.org/wiki/ISO_8601" target="_blank">ISO 8601</a> standard. This encodes the time as follows: <br><br><ul><li>Combined date and time in UTC: 2013-06-10T10:00Z</li><li>Combined date and time in localtime with the timezone offset: 2013-06-10T12:00+02:00</li><li>Combined date and time in localtime with the timezone offset: 2013-06-10T07:00-03:00</li></ul> The examples refer all to the same time.</p>
<div></details>
</section></li>
</ul>
<div></details>
</section></li>
</ul>
