# codeformuenster.org

This repository contains the source code of our homepage [opendata-nuernberg.github.io](https://opendata-nuernberg.github.io/).

The site is being built with [jekyll](https://jekyllrb.com/) and is hosted on [GitHub Pages](https://pages.github.com/).

Our site is based on the excellent work of [codeformuenster.org](https://codeformuenster.org) and started with an forked. So we're also using the theme called [bulma-clean-theme](https://github.com/chrisrhymes/bulma-clean-theme) with some modifications made by [codeformuenster.org](https://codeformuenster.org). The original theme is created by [Chris Rhymes](https://www.csrhymes.com/) and is licensed under the [MIT license](https://github.com/chrisrhymes/bulma-clean-theme/blob/master/LICENSE.txt)

## Development

```bash
    # Using docker-compose (recommended, but is currently not working)
    sudo docker-compose up
```

```bash
    # Using docker for debugging purpose
    docker run -it --rm -v $(pwd):/srv/jekyll -p4000:4000 jekyll/jekyll bash
    # install bundle 
    bundle install
    # start webserver
    bundle exec jekyll serve --force_polling -H 0.0.0.0 -P 4000
    # start webserver with file watch
```

docker run -it --rm -v /Users/jsi/src/opendata/opendata-nuernberg.github.io/.:/srv/jekyll -p4000:4000 jekyll/jekyll bash


jekyll new --skip-bundle .

# only once, to add webrick to the Gemfile
# bundle add webrick

bundle install
bundle exec jekyll serve --force_polling -H 0.0.0.0 -P 4000

-w watch


### I want to add an image to the front page carousel

- Add your image to `assets/img/carousel`
- Add the filename to the `carousel_images` array in `index.md`
- Change the `$numberOfImgs` variable in `assets/css/app.scss`

### I want to add a project

- Open `_data/projects.yaml`
- Add your project in the following form

      repositoryname:
        title: The title of the project
        project_url: The url of the project (optional github project url will be used if missing)
        image: the file name of the project image. File should be in assets/img/projects
        showcased: true/false

- If your project should be showcased, add an image to assets/img/projects

### I want to add a blog post

- Create a new file in the `_posts` directory with filename `YYYY-MM-DD-title.md`
- The date `YYYY-MM-DD` represents the blog posts publishing date
- Your post should start with a frontmatter like this:

      ---
      layout: post
      title: Open Data Day 2018 in Nürnberg
      author: Anthony Author
      twitter: your_twitter_handle
      category: blog
      ---

- Future posts won't be rendered on the live page

### I want to add an event

- Open `_data/events.yaml`
- Add event in the format of the other events
- Only next 4 events will be shown
- Events older than today will automatically disappear as soon as the github-page is regnerated (e.g. after a PR is merged)

### I want to add a press article

- Open `_data/presse.yaml`
- Add the article in the following form


      - wann: YYYY-MM-DD
        wer: Káseblatt des Westens
        thema: Lobhudelei der Open-Data-Schergen aus Nürnberg
        link: https://kaseseblatt.org/posts/codefornuernberg-ist-einfach-toll
