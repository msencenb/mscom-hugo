---
title: "Rails 4 and Paperclip with S3 + Cloudfront"
date: "2016-04-21"
categories: 
  - "software engineering"
---

It's been over two years since I have implemented [Paperclip](https://github.com/thoughtbot/paperclip), the awesome image attachment gem, into a Rails app. The [basic setup](https://github.com/thoughtbot/paperclip#quick-start) is still very easy and clean to do, as is the initial setup to get S3 storage working.

But what's not well documented is how to use [Cloudfront](https://aws.amazon.com/cloudfront/) to serve up your image attachments rather than pulling them from [S3](https://aws.amazon.com/s3/). Thanks to this helpful [answer on stack overflow](http://stackoverflow.com/questions/32077746/rails-4-use-cloudfront-with-paperclip), and a little digging into the code of Paperclip itself, it turns out to be trivial to implement. All you need to do is setup your url and s3\_host\_alias properly in your configuration files. Here's what my production.rb config file now looks like for Paperclip:
````
  config.paperclip\_defaults = {
      storage: :s3,
      url: ":s3\_alias\_url",
      path: "/:class/:attachment/:id\_partition/:style/:filename",
      s3\_host\_alias: "xxxxxx.cloudfront.net",
      s3\_credentials: {
          bucket: ENV\['S3\_BUCKET\_NAME'\],
          access\_key\_id: ENV\['AWS\_ACCESS\_KEY\_ID'\],
          secret\_access\_key: ENV\['AWS\_SECRET\_ACCESS\_KEY'\]
      }
  }
``
 

Enjoy!
