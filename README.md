## Build

`jekyll build` builds the site and outputs the result to `_site`

`jekyll serve` does the same thing, and additionally rebuilds upon any change, serving the site locally (typically on port `4000`)

## Deployment

This application uses the following plugins, which are not supported by GitHub Pages:

- [jekyll-paginate-v2][jekyll-paginate-v2]

For this reason, simply updating and pushing the pre-compiled code will correctly update the site. GitHub Pages builds the application, and the features provided by unsupported plugins won't be available. Therefore, a hook has been defined in `.git/hooks/pre-push`, as documented by [Nicu Surdu][pre-push]. This builds the application and places the result in the `gh-pages` branch. The repository is configured to deploy this branch.

## Folder Structure
- _data: custom [data][data]
- _includes: content to [include][include] in multiple places
- _pages: individual pages
    - exploration: pages for explorations
        - easterncontinentaltrail: pages for the 2012 Eastern Continental Trail trip
            - journal: pages for the journal for the 2012 Eastern Contentail Trail trip
                - april: april journal entries
                - august: august journal entries
                - february: february journal entries
                - january: january journal entries
                - july: july journal entries
                - june: june journal entries
                - march: march journal entries
                - may: may journal entries
- _posts: posts to be displayed in a blog post format
    - blog: posts for the blog
- assets: assets to be loaded
    - css: style sheets to be loaded

[data]: https://jekyllrb.com/docs/datafiles/
[include]: https://jekyllrb.com/tutorials/convert-site-to-jekyll/#9-simplify-your-site-with-includes
[jekyll-paginate-v2]: https://github.com/sverrirs/jekyll-paginate-v2
[pre-push]: https://surdu.me/2020/02/04/jekyll-git-hook.html