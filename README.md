#### Local Preview
The website should be previewed locally before pushing any changes.  
Perform the following steps for the initial setup:
* `ruby --version`  
  Check whether you have Ruby 2.1.0 or higher installed on your system.
* `gem install bundler`  
  [Bundler](https://bundler.io/) is used to manage the gems needed to build the website.
* `bundle install` In the root directory of the Repository.  
  Install all gems needed to build the website.
  
The following command only has to be restarted if the `_config.yml` file is changed.
  
* `bundle exec jekyll serve` In the root directory of the Repository.  
  Generate the website and make it available on `http://127.0.0.1:4000`.
  
#### Updating Gems
Execute `bundle update` in the root directory of the Repository. This will update `Gemfile.lock` to require the latest versions of all gems the website uses.

 