# Harvard Art Museums blog

This blog uses Jekyll, a static site generator, to publish on GitHub pages. It is setup using a fork of the Jekyll Now project by Barry Clark. Any custom features and templates will be listed here as they are developed.

## Setup for local development 

There were some issues with the Jekyll Now local setup instructions, but feel free to try the quick setup under Jekyll Now instructions first before the ones directly following:

1. Install chruby and Jekyll: `https://jekyllrb.com/docs/installation/macos/
2. Install and use Bundler: `https://jekyllrb.com/tutorials/using-jekyll-with-bundler/`
3. clone repo: `https://github.com/harvardartmuseums/blog`
4. Update the _config.yml file by copy and pasting from the repo but exclude the base path setting of `/blog`
5. Serve the site and watch for markup/sass changes `jekyll serve`
6. View your website at http://127.0.0.1:4000/


# Instructions from Jekyll Now

## Local Development (Quick Setup)

1. Install Jekyll and plug-ins in one fell swoop. `gem install github-pages` This mirrors the plug-ins used by GitHub Pages on your local machine including Jekyll, Sass, etc.
2. Clone down your fork `git clone https://github.com/yourusername/yourusername.github.io.git`
3. Serve the site and watch for markup/sass changes `jekyll serve`
4. View your website at http://127.0.0.1:4000/
5. Commit any changes and push everything to the master branch of your GitHub user repository. GitHub Pages will then rebuild and serve your website.

## Moar!

I've created a more detailed walkthrough, [**Build A Blog With Jekyll And GitHub Pages**](http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/) over at the Smashing Magazine website. Check it out if you'd like a more detailed walkthrough and some background on Jekyll. :metal:

It covers:

- A more detailed walkthrough of setting up your Jekyll blog
- Common issues that you might encounter while using Jekyll
- Importing from Wordpress, using your own domain name, and blogging in your favorite editor
- Theming in Jekyll, with Liquid templating examples
- A quick look at Jekyll 2.0’s new features, including Sass/Coffeescript support and Collections