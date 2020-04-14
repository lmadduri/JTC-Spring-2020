
<a id="domains"></a>
### Customizing your domain

To customize your website's domain name, it's as easy as 1, 2, 3i, 3ii!

1.  Go to [Namecheap](https://namecheap.com) and buy a domain you like!
    Remember, the [GitHub student developer
    pack](https://education.github.com/pack/) comes with a free
    `.me` domain from Namecheap, in case you don't want to
    spend any money.
2.  In your `username.github.io` repo, at the same level
    as `index.html`create a file called
    `CNAME`. Inside that file, add just one line: your new
    domain name, all lowercase, and nothing else. For example, if you buy `coolperson.me`, your
    site's CNAME is just:

        coolperson.me

3.  In Namecheap, in your dashboard, click “Manage” on the domain name
    you just bought. Then click on Advanced DNS from the tabs in the
    middle of the page. Then, do the following:

    1.  Use the red “Add new record” button to add two A Records, both
        with host `@`, one with the IP address
        `192.30.252.153`, the other with IP address
        `192.30.252.154`.
    2.  Use the red “Add new record” button to add a CNAME Record, with
        host `www` and the value
        `[username].github.io.`.
        Don't
        leave out the dot at the end of it!

You'll need to wait at least half an hour for the changes to finish, but
after that, everything should work like you want it to.

<a id="responsive"></a>
### CSS Media Queries

While you were designing your website, did you ever think about what it
would look like on a phone? More and more people browser the internet
using their phones, and it's our duty as web developers to make sure our
websites' user experience is just as good on a phone or tablet.

The best way to do this is in your CSS, with **media queries**! That's
how this website looks passable on mobile.

-   [Here](http://learnlayout.com/media-queries.html)'s a
    quick introduction.
-   [Here](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)'s
    a great reference guide.
-   [Here](https://css-tricks.com/logic-in-media-queries/) are some
    interesting tricks if you want to get your brain working hard.

<a id="favicons"></a>
### Favicons

Ever wonder how there's a little green J next to the
`title` in your browser's tabs? It's called a **favicon**,
and all the cool kids will have one on their personal sites.

You can make one with [this silly tool](http://www.favicon.cc/), and
store it at the same level as your `index.html` with the
name `favicon.ico`.

To use a `.png`, or to get more information about the
rabbit hole that is the favicon, check out this [incredibly detailed
guide](https://github.com/audreyr/favicon-cheat-sheet). Don't spend too
much time there or your brain will explode.

<a id="ga"></a>
### Google Analytics

Why make a personal site if you can't have incredibly detailed
information about how many people are visiting your website every day,
where they're from, and what browser they're using? [Google
Analytics](https://google.com/analytics) is such a comically useful tool
that every time I use it I'm amazed at how free it is.

The guide on the Google Analytics site should be enough to get you
started;
[here](https://support.google.com/analytics/answer/1008015?hl=en) is an
extra-detailed guide in case you get stuck.

<a id="bootstrap"></a>
### Bootstrap

I love web design, but I recognize that not everyone shares my love for
wrangling with CSS. If that sounds like you, you should check out
[Bootstrap](https://getbootstrap.com): it's a **CSS framework**, which
provides a lot of built-in styling that works well on all devices.

-   [Here](https://www.codecademy.com/courses/web-beginner-en-yjvdd/0/1)
    is a great way to get started with Bootstrap: a lesson from
    Codecademy!
-   [Here](https://getbootstrap.com/getting-started/)'s Bootstrap's own
    “getting started” guide.
-   [Here](https://www.youtube.com/watch?v=YXVoqJEwqoQ)'s a pretty
    reasonable (if slightly out of date) video guide to getting started
    with Bootstrap.
