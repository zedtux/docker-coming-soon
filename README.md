# Docker Coming-soon

When you need a "coming soon" page but you have no time to build one.

I took [this free template](http://www.creative-tim.com/product/coming-sssoon-page)
made by [Creative Tim](http://www.creative-tim.com/).
I have cleaned the code and written an interpolation script which allows you to
configure it quickly using environment variables.
Finally I put this in the Docker image [zedtux/docker-coming-soon](https://hub.docker.com/r/zedtux/docker-coming-soon/)
allowing you to run it easily.

Here is an example of the result:

![coming-soon](https://cloud.githubusercontent.com/assets/478564/20465730/cee8570e-af64-11e6-996c-bb8ef24b2bdd.png)

# Usage

You have the following environment variables which allow you to configure the
coming soon page:

| Variable name | Description                           | Example                                                                |
|-----------------|-------------------------------------------|---------------------------------------------------------------------------------|
| TITLE         | Webpage head title                   | TITLE="Awesome App"                                                    |
| PRODUCT_NAME  | Product name show on the page        | PRODUCT_NAME="My Awesome App"                                          |
| CATCHY_PHRASE | The sentence under the product name  | CATCHY_PHRASE="Awesome App is what you were looking for since a while." |
| FACEBOOK_URL  | Facebook button URL to your page     | FACEBOOK_URL="https://www.facebook.com/awesomeapp"                     |
| TWITTER_URL   | Twitter button URL to your page      | TWITTER_URL="https://www.twitter.com/awesomeapp"                       |
| GITHUB_URL    | Github button URL to your page       | GITHUB_URL="https://www.github.com/awesomeapp"                         |
| EMAIL         | Email to be used for the Email button | EMAIL="me@mydomain.com"                                                |

Run the image with the following:

```bash
docker run --name coming-soon -d -p 80:80 -e TITLE="Awesome App" -e PRODUCT_NAME="My Awesome App" zedtux/docker-coming-soon
```

Now you should be able to access it.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
