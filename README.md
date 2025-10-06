# app-on-homescreen-apple-not-caching-or-buffering

An iPad is a real great tablet, also for "older people". Not many things you can do wrong, so they love working with it.

In Holland you have radio-stations which broadcast online, e.g. NPO Radio 5. They provided an app, which worked great, but they removed it from the app-store, to use a "combined app". Which does not work great, especially for "elder people".

So you browse to the website in Safari or Chrome and add a shortcut to the site on the homescreen of the iPad. 

The "older person" only has to click on that shortcut, click on the Play-button in the website and you are "ready to go".


Well, not really. To stop playing, you press the "stop" button (is the same button as the play-button, but when you play it updated to a stop icon).

The user closes the screen and opens "the app again" the next day. But, Apple does not really close screens, it just hides them. So you open the hidden screen and when you press the play button it continues at the time you stopped playing. Or some other things went wrong with the buffering.

So you should dispose the screen, which is quite difficult for older people and you get tired of the complaints. How can we fix this?


# My solution

First you place the page-initial.php as "[page].php" on your hosting. You open this page and place it on the homescreen of the iPad.

Then you replace "[page].php" file on your hosting with page-final.php. This file contains a meta-header which redirects you to the desired page in 1 second.

Because the headers returned indicate that "you may/shall not cache this page", every time your page is requested it redirects you to the target page. So it will never be buffered.

[page].php is an example name. In my case it was about the [page of NPO Radio 5](https://www.nporadio5.nl/), so I called it npo-radio5.php

In the pages you have to replace [TARGET-URL] with the URL you want the page to be directed to, [COOL-IMAGE] with the filename of the image you want to appear on the homescreen of the iPad and in the page.