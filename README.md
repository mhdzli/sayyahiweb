Based on [Galada](https://artemsheludko.github.io/galada/) an easy and simple theme for Jekyll.

# Substantial modifications:

* Awsome Font Icons instead of Ionicons Icons
* Persian Jalali Date
* Vazir font
* Remove Disqus comments


* * *

# Deployment

To run the theme locally, navigate to the theme directory and run `bundle install` to install the dependencies, then run `jekyll serve` or `bundle exec jekyll serve` to start the Jekyll server.

I would recommend checking the [Deployment Methods](https://jekyllrb.com/docs/deployment-methods/) page on Jekyll website.

* * *

# Posts

To create a new post, you can create a new markdown file inside the \_posts directory by following the [recommended file structure](https://jekyllrb.com/docs/posts/#creating-post-files).

      ---
      layout: post
      title: Premiere on Broadway
      date: 2018-08-23 16:04:00 +0300
      image: 03.jpg
      tags: [Rest]
      ---
          

You can set the tags and the post image.

Add post images to **/img/** directory.

For tags, try to not add space between two words, for example, `Ruby on Rails`, could be something like (`ruby-on-rails`, `Ruby_on_Rails`, or `Ruby-on-Rails`).

* * *

# Instagram

The Instagram feed is working using [Instafeed.js](http://instafeedjs.com/) to show the photos.

First, you will need to get your account `userId` and `accessToken` from the following URLs:

*   userId: [smashballoon.com/instagram-feed/find-instagram-user-id](https://smashballoon.com/instagram-feed/find-instagram-user-id/)
*   accessToken: [instagram.pixelunion.net](http://instagram.pixelunion.net/)

Second, open the `js/common.js` file and replace the `userId` and `accessToken` values.

            var instagramFeed = new Instafeed({
              get: 'user',
              limit: 6,
              resolution: 'standard_resolution',
              userId: '8987997106',
              accessToken: '8987997106.924f677.8555ecbd52584f41b9b22ec1a16dafb9',
              template: ''
            });
          

Third, open the `_config.yml` file and replace the `instafeed: false` on `instafeed: true` value.

            \# Instagram Feed
            instafeed: false \# To enable the instafeed, use the value true. To turn off use the value false.
          

* * *

# Google Analytics

To integrate Google Analytics, open `_config.yml`, and add your Google Analytics identifier.

    \# Google Analytics
    google-analytics: \# Add your identifier. For example UA-99631805-1
          

* * *

### Update favicon

You can find the current favicon (favicon.ico) inside the theme root directory, just replace it with your new favicon.

* * *

# License

Mit License

