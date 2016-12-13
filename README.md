# open-austin.org

### The Open Austin website

- [How to Draft a Blog Post](https://github.com/open-austin/open-austin.github.io/wiki/How-to-Draft-a-Blog-Post)
- [Development Instructions](#development-instructions)
- [Planning](#planning)
- [License](#license)

------------------

# Development Instructions

## Installing Jekyll/Ruby on OS X
- *(Optional)* Install [**iTerm**](https://www.iterm2.com/) for a better Command Line App in OS X.

- _(Optional)_ Install [**oh-my-zsh**](https://github.com/robbyrussell/oh-my-zsh
) for a prettier command line interface and easier zsh configuration than bash.
	- `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

- Install [**homebrew**](http://brew.sh/) (for better installation of OS X packages)
	- `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

- Install [**ruby-install**](https://github.com/postmodern/ruby-install#readme) for installing Ruby versions. (OS X comes with 2.0.0, but its not the latest version and you may have to use the `sudo` command to do anything. Best to install a version manager like ruby-install + chruby to help with that.)
	- `brew install ruby-install`
	- `ruby-install ruby 2.2.2`

- Install [**rvm**](https://rvm.io/) to switch ruby versions.
	- `gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3`
	- `\curl -sSL https://get.rvm.io | bash -s stable`
	- `rvm use 2.2.2`

- Install [**jekyll**](https://jekyllrb.com/) to install Jekyll.
	- `gem install jekyll`

## Start Jekyll

Once you've got everything installed, run

```
jekyll serve --incremental --watch --trace
```

Then go to

```
http://localhost:4000/
```


### Instructions for exporting content from Wordpress

```
gem install jekyll-import hpricot open_uri_redirections
ruby -rubygems -e 'require "jekyll-import";
    JekyllImport::Importers::WordpressDotCom.run({
      "source" => "import/openaustin.wordpress.2015-11-21.xml",
      "no_fetch_images" => false,
      "assets_folder" => "assets"
    })'
```

--------------------

# Planning

Staging Site: http://open-austin.github.io/

## Planning & Design
### Sitemap

![our sitemap](planning-design/site_architecture/oa-sitemap.png?raw=true)
[link to Gliffy](http://www.gliffy.com/go/publish/8981187)

### Design Docs
[Design Brief](planning-design/planning_and_analytics/OA Design Brief.pdf?raw=true)

[Colors/Typography](planning-design/typography/colorstypography2.png?raw=true)

### Mockups
[Homepage Mockups from 1-Sept](planning-design/final_mockups/oa_homepage_mockup.pdf?raw=true)

Higher fidelity Mockup from 24-Aug Meeting ([PDF](planning-design/other_mockups/OA Homepage 1.pdf?raw=true) AND [Sketch](planning-design/other_mockups/OA Homepage 1.sketch?raw=true))

[Original Lo-fi Mockup](planning-design/planning_and_analytics/lo-fi-mockup.jpg?raw=true)

### Requirements
[Link to functional requirements doc](https://docs.google.com/document/d/1dgYQunemFzfGPpmc6jJz5L1sCm0m7f9ZemPT0z6FK2c)

### Assets/Images
[Links to potential assets/images](https://github.com/open-austin/OA-Website/wiki/Assets-&-Images-for-potential-use)

# License

The code for this repository has been released into the public domain by Open Austin via the Unlicense.
