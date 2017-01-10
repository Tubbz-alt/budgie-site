# Budgie Site

Static, [Hugo-based](https://gohugo.io) home of Budgie Desktop. This website makes used of:

1. A custom theme, in `themes/budgie`.
2. Custom layouts and importable "fragments" for separation and modularizing of common components, within `layouts`.
3. Website content itself, including blog posts, in `content`.

**This does not include the LESS-based styling for the website. That is developed separately at the [budgie-site-styling repo](https://github.com/budgie-desktop/budgie-site-styling).**

## Creation

### New Post

To create a new post, call `hugo new PATH`. For instance, `hugo new blog/welcome-to-the-new-site.md` would create `welcome-to-the-new-site.md` with our default
configuration in the `content/blog/` directory.

## Development

### Setup

To set up your Solus system for the website development, you first need to ensure you have the necessary dependencies installed. Run `make setup` to install the necessary dependencies as well as 
init git submodules. If you're not on Solus, make sure to install `hugo` 0.18.1 or above.

Next, run `make sync` to sync the latest CSS and JS and ensure they are copied over the appropriate directories.

### Local Server

You can start up a local server by calling `make local` in the `budgie-site` directory. This will expose the site on `http://127.0.0.1:1313/home`.

**Note:** You will not need to restart the server when doing changes. Hugo does file watching across all the things.

### Deployment

To compile the website in preparation for deployment, run `make deploy`. This will create a `public-deployed` folder which can be uploaded to the server. Make sure you run a `make sync` prior to deployment, 
to ensure you have the latest CSS and JS.

**Note:** This really only applies to the Budgie Desktop website administrators but since the Make recipe exists, may as well document it.

### Benchmarking

You can easily benchmark Hugo compilation by running `make benchmark`. You will get an output similar to:

```
Average time per operation: 170ms
Average memory allocated per operation: 114037kB
Average allocations per operation: 1299640
```

### Styling

I use 4-char wide tabs, not spaces, in everything **except** the YAML files. I know, I'm a monster.

## Licensing

Apache 2.0