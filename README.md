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
* The `_data` folder contains YAML files in which data for the generation of the website is stored.
* The `_layouts` folder contains the `default.html` template which is used to generate all pages of the website.
* The `assets` folder contains subfolders in which all assets for the website are to be placed. 
  All CSS files sould be placed in `assets/css`. The `style.scss` is used to generate CSS which is applied to all pages.
  All images should be placed in `assets/img`.
* The `pages` folder contains the Markdown files used to generate the pages of the website. 
  The `_config.yml` contains directives causing these files to be rendered into HTML pages under the root of the website.

#### Adding a Steering Committee Member
To add (or remove) a steering committee member, the file `_data/steering_committee.yml` has to be modified.
The file contains a list of [YAML](https://en.wikipedia.org/wiki/YAML) dictionaries describing the members of the steering committee.
For every member a section of the following form has to be added:

    - firstname: <firstname>
      lastname: <lastname> 
      image: <path relative to assets/img> 
      homepage: <link>
      affiliation: <affiliation>
      position: <position>

The entries in `steering_committee.yml` will be rendered as a table in the `pages/steering_committee.md` file. They will be ordered by the value of the `lastname` field.

#### Adding an Event
To add (or remove) an event, the files `_data/events_previous.yml` or `_data/events_upcoming.yml` have to be modified for previous or upcoming events respectively.
The file contains a list of [YAML](https://en.wikipedia.org/wiki/YAML) dictionaries describing the events.
For every event a section of the following form has to be added:

    - name: <name>
      link: <link>
      location: <location>
      year: <year>
      category: <category>

The entries in the data files will be grouped by `category` and rendered as tables in the `pages/past_events.md` and `pages/upcoming_events.md` files. The events in each category will be ordered by their `year`.

#### Updating Gems
Execute `bundle update` in the root directory of the Repository. 
This will update `Gemfile.lock` to require the latest versions of all gems the website uses. 
Please ensure that no Windows specific gems are committed.
