# AE 370

This repository hosts the AE 370 course website.

## Website

### Set Up and Installation

This website is built using [Jekyll](https://jekyllrb.com/), hosted on [GitHub](https://github.com/), and served by [GitHub Pages](https://pages.github.com/). The site uses the [Just the Docs](https://just-the-docs.github.io/just-the-docs/) theme.

The website was created using the following steps.

1. [Create](https://pages.github.com/) a repository for the site on GitHub. The repo was set up for a "User or organization site".

1. [Install](https://jekyllrb.com/docs/) Jekyll and create a new Jekyll site in the repo. See the note about adding `webrick`.

    ```
    gem install jekyll bundler
    jekyll new .
    ```

1. [Install](https://just-the-docs.github.io/just-the-docs/) the Just the Docs theme. The theme was installed as a [GitHub Pages remote theme](https://just-the-docs.github.io/just-the-docs/#quick-start-use-as-a-github-pages-remote-theme) for this site, which also required updating [`Gemfile`](Gemfile) to use GitHub Pages.

1. You should now be able to build the site make it available on a local server.

    ```
    bundle exec jekyll serve
    ```

    Browse to [http://localhost:4000/](http://localhost:4000/).

### Customization

The schedule was created using files from the [Just the Class](https://kevinl.info/just-the-class/) theme. Specifically, the `/_sass/`, `/_layouts/`, `/staffers/`, and `/_modules/` files were based on corresponding [files](https://github.com/kevinlin1/just-the-class) from that theme.

## GitHub Classroom

### Creating a Classroom

I maintain a main organization (e.g., "uiuc-ae370") and separate classroom organizations for each semester (e.g., "uiuc-ae370-2022-fall") to prevent the main organization from being filled with student assignment repositories. The main organization stores main assignment repositories (e.g., including solutions, etc.). The classroom organizations store assignment repositories actually distributed to students for a given semester and student versions of those repositories.

I use the following process to create a GitHub Classroom:

1. Go to [https://classroom.github.com/classrooms](https://classroom.github.com/classrooms) and click the "New classroom" button.

    Make sure you are signed in to the GitHub account you want to use for the classroom.

1. Click the "Create an organization" button or click the existing organization you want to use for the classroom. Set up and then select the organization if needed.

1. Name the classroom.

    I typically use the same name as the associated classroom organization (e.g., "uiuc-ae370-2022-fall").

1. Add [instructors](#managing-instructors) and/or [students](#managing-students) (you can always do this later).

### Managing Instructors

### Managing Students

Add students to the classroom by doing the following:

1. Add students to the GitHub Classroom roster (e.g., using a `.csv` of Netids). Student identifiers are independent of the GitHub account they use.
1. Give an assignment link to the students to have them join the classroom.

    Once they click the link for their first assignment, they will be asked to join the classroom by selecting the identifier that matches themselves. This will link their GitHub account to the identifier in the GitHub Classroom roster.
    
    Make sure they are signed in to the GitHub account they want to use when they click the link. Students will need to Authorize GitHub Classroom permissions for their GitHub account.

Students will only be able to see their own assignment repositories (unless assignments were made public).

### Creating and Distributing Assignments

1. Create (or update) a repository for the assignment in the main organization for the course (e.g., "uiuc-ae370/hw1-python-refresher").

    I include all relevant files in this repository, including solutions and the files students will actually be given. I keep these repositories private so students cannot access solutions.

1. Fork (or pull) the assignment repository from the main organization to the GitHub Classroom organization used for the current semester (e.g., "uiuc-ae370-2022-fall/hw1-python-refresher").

    The forked repository will be used as a template for the assignment in GitHub Classroom. You may need to [adjusting settings](https://docs.github.com/en/organizations/managing-organization-settings/managing-the-forking-policy-for-your-organization) for the main organization to enable forking of private repositories.

1. Update the forked repository (e.g., "uiuc-ae370-2022-fall/hw1-python-refresher") to only include files students should have access to in their assignment (e.g., removing solution files).

    Make sure to push changes to the repository on GitHub. My typical process is:

    ```
    # clone repository locally
    cd ../ae370-2022-fall
    git clone https://github.com/uiuc-ae370-2022-fall/hw1-python-refresher.git

    # delete `hw1-python-refresher-solution.ipynb
    # delete `tutorial-figure.png`

    # commit changes
    git status
    git add .
    git commit -m "remove solution files"

    # push changes to GitHub
    git push
    ```

1. Make the forked repository a "Template repository" (Settings -> General -> Template Repository).
1. Go to GitHub Classroom and click the "New assignment" button.

    I typically grant students admin access so they can add other users as collaborators.

1. Select the forked repository (e.g., "uiuc-ae370-2022-fall/hw1-python-refresher) in the "Add a template repository to give students start code" section.

    Assignments created from a template repository will start with a single commit (i.e., they will not include the entire commit history of the template repository).

1. Give students access to the assignment using the assignment link.

    Once they click the link for the assignment, an assignment repository (with their user name appended to the end) will be created for them in the GitHub Classroom organization.

## Contact

Feel free to contact Huy Tran (huytran1@illinois.edu) with any questions!
