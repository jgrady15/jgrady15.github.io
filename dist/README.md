### Building website

Using the UI

```sh
$ gitfolio ui
```

> Tip: You can use ui to create new blogs and for updating your folio too.

or

```sh
gitfolio build <username>
```

`<username>` is your username on github. This will build your website using your GitHub username and put it in the `/dist` folder.

To run your website use `run` command, Default port is 3000

```sh
gitfolio run -p [port]
```

### Let's Customize

#### Sorting Repos

To sort repos provide `--sort [sortBy]` argument while building. Where `[sortBy]` can be `star`, `created`, `updated`, `pushed`,`full_name`. Default: `created`

```sh
$ gitfolio build <username> --sort star
```

#### Ordering Repos

To order the sorted repos provide `--order [orderBy]` argument while building. Where `[orderBy]` can be `asc` or `desc`. Default: `asc`

```sh
$ gitfolio build <username> --sort star --order desc
```

#### Customize Themes

Themes are specified using the `--theme [theme-name]` flag when running the `build` command. The available themes are

- `light`
- `dark`

> TODO: Add more themes

For example, the following command will build the website with the dark theme

```sh
$ gitfolio build <username> --theme dark
```

#### Customize background image

To customize the background image just provide `--background [url]` argument while building

```sh
$ gitfolio build <username> --background https://images.unsplash.com/photo-1557277770-baf0ca74f908?w=1634
```

You could also add in your custom CSS inside `index.css` to give it a more personal feel.

#### Add Social Media links on your profile

Twitter, LinkedIn, Medium & Dribbble links to your profile while building

```sh
gitfolio build <username> --twitter <twitter_username> --linkedin <linkedin_username> --medium <medium_username> --dribbble <dribbble_username>
```

### Updating

To update your info, simply run

```sh
$ gitfolio update
```

or use the `Update` options in gitfolio's UI

This will update your info and your repository info.

To Update background or theme you need to run `build` command again.

### Add a Blog

To add your first blog use the UI.

```sh
$ gitfolio ui
```

This will open up a UI page and you can click on `New Blog` to create a new blog. Once you are done writing your blog you can hit the `Create Blog`.

This will create a blog inside `./dist/blog` folder.

Look for success or error in your terminal.

This also adds content to `blog.json` file. This file helps in showcasing your blogs on your personal website as [cards](https://imfunniee.github.io/gitfolio/#blog_section). You could customize the JSON object that corresponds your current blog.

Blog Demo? [here](https://imfunniee.github.io/gitfolio/blog/my-first-post/)

Blog's default JSON Format

```
{
  "url_title": "my-first-blog", // the title you provide while creating a new blog, this appears in url
  "title": "Lorem ipsum dolor sit amet", // main title of blog
  "sub_title": "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", // sub-title of blog
  "top_image": "https://images.unsplash.com/photo-1553748024-d1b27fb3f960?w=1450", // main image of blog
  "visible": true // don't worry about this
}
```
### Credit to template: [@imfunnieee](https://twitter.com/imfunnieee)

### Their template license

![GitHub](https://img.shields.io/github/license/imfunniee/gitfolio.svg?style=popout-square)
