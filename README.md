Welcome to the Web site of the ACM Joint European Software Engineering Conference and Symposium on the Foundations of Software Engineering (ESEC/FSE).

#### Technology
This website is developed using the [Jekyll](https://jekyllrb.com/) static site generator and hosted using [GitHub Pages](https://pages.github.com/). 
The current state of the `master` branch is always available under [https://esec-fse.github.io/](https://esec-fse.github.io/).

### Development
To prevent accidental modification of the live website, the `master` branch is protected. 
Please create development branches for any proposed changes to the site. 
Once you believe your changes should go live, issue a [pull request](https://help.github.com/articles/about-pull-requests/) from your branch into `master` and assign an appropriate reviewer.

#### Local Preview
The website should be previewed locally before issuing pull requests.  
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
  
#### Files and Folders
* The root folder of the repository only contains files necessary for the configuration of Jekyll or the repository in general.
* The `_layouts` folder contains the `default.html` template which is used to generate all pages of the website.
* The `assets` folder contains subfolders in which all assets for the website are to be placed. 
  All CSS files sould be placed in `assets/css`. The `style.scss` used to generate CSS which is applied to all pages.
  All images should be placed in `assets/img`.
* The `pages` folder contains the Markdown files used to generate the pages of the website. 
  The `_config.yml` contains directives causing these files to be rendered into HTML pages under the root of the website.

#### Updating Gems
Execute `bundle update` in the root directory of the Repository. This will update `Gemfile.lock` to require the latest versions of all gems the website uses. Please ensure that no Windows specific gems are committed.
