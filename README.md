# AE 370

This repository hosts the template for the AE 370 course website.

## Creating a website for a new semeseter

The website is built using [Jekyll](https://jekyllrb.com/), hosted on [GitHub](https://github.com/), and served by [GitHub Pages](https://pages.github.com/). The site uses the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) theme. We use the following steps to create a new website each semester using past templats.

1. Create a template repository for the website using the [Just the Docs Template](https://just-the-docs.com/#getting-started). Put the repository in the organization for the new semester (e.g., "uiuc-ae370-2023-fall") and name it using the [expected GitHub pages repo name](https://pages.github.com/) (e.g., "uiuc-ae370-2023-fall.github.io").

1. Clone the template repo.

    ```
    # clone repository locally
    $ cd ../ae370-2023-fall
    $ git clone https://github.com/uiuc-ae370-2023-fall/uiuc-ae370-2023-fall.github.io.git
    ```

1. Install [Jekyll](https://jekyllrb.com/docs/installation/) and Bundler if needed. You might need to make sure the correct ruby version is being used. I installed [rbenv](https://github.com/rbenv/rbenv) to manage my ruby version.

    ```
    # check if jekyll is installed
    $ jekyll -v

    # check if bundler is installed
    $ bundler -v
    ```

1. Build and preview the site locally to make sure the template works.

    ```
    # change your working directory to the root directory of the site
    $ cd ../ae370-2023-fall/uiuc-ae370/2023-fall.github.io

    # install project dependencies
    $ bundle install

    # build local site
    $ bundle exec jekyll serve
    ```
    Browse to [http://localhost:4000/](http://localhost:4000/).

1. Copy desired files from this repo into the new site repo. I usually copy the following:

    - _layouts/
    - _modules/
    - _sass/
    - _staffers/
    - assets/
    - docs/
    - _config.yml
    - .gitignore
    - environment.yml
    - index.md

1. Build and preview and site again. You might need to exit terminal before doing so.

    ```
    # build local site
    $ bundle exec jekyll serve
    ```
    Browse to [http://localhost:4000/](http://localhost:4000/).

1. Then just update files as needed. The website should automatically update when you push changes on the main branch.

## Customization

The schedule was created using files from the [Just the Class](https://kevinl.info/just-the-class/) theme. Specifically, the `/_sass/`, `/_layouts/`, `/staffers/`, and `/_modules/` files were based on corresponding [files](https://github.com/kevinlin1/just-the-class) from that theme.

## Contact

Feel free to contact Huy Tran (huytran1@illinois.edu) with any questions!
