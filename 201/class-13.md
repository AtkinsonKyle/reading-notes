# Daily Reading 13
## Local Storage
<hr>

### Things To Know
- Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data.
  - Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
  - Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
  - Cookies are limited to about 4 KB of data — enough to slow down your application, but not enough to be terribly useful
- userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure.
- In 2002, Adobe introduced a feature in Flash 6 that gained the unfortunate and misleading name of “Flash Cookies” The feature is properly known as Local Shared Objects.
- Brad Neuberg developed an early prototype of a Flash-to-JavaScript bridge called AMASS (AJAX Massive Storage System), but it was limited by some of Flash’s design quirks.
- The Indexed Database API exposes what’s called an object store. An object store shares many concepts with a SQL database.