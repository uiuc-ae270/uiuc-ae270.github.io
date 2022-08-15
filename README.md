# Course Website

This repository hosts the AE 370 course website.

## Set Up and Installation

This website is built using [Jekyll](https://jekyllrb.com/), hosted on [GitHub](https://github.com/), and served by [GitHub Pages](https://pages.github.com/). The site uses the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) theme.

The website was created using the following steps.

1. [Create](https://pages.github.com/) a repository for the site on GitHub. The repo was set up for a "User or organization site".

1. [Install](https://jekyllrb.com/docs/) Jekyll and create a new Jekyll site in the repo. See the note about adding `webrick`.

1. [Install](https://just-the-docs.github.io/just-the-docs/) the Just the Docs theme. The theme was installed as a [GitHub Pages remote theme](https://just-the-docs.github.io/just-the-docs/#quick-start-use-as-a-github-pages-remote-theme) for this site, which also required updating [`Gemfile`](Gemfile) to use GitHub Pages.

1. You should now be able to build the site make it available on a local server.

    ```
    bundle exec jekyll serve
    ```

    Browse to [http://localhost:4000/](http://localhost:4000/).

## Contact

Feel free to contact Huy Tran (huytran1@illinois.edu) with any questions!