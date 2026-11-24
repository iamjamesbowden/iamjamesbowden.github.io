# jwbowden.com

Personal academic website for James Bowden, built with Jekyll and hosted on GitHub Pages at <https://www.jwbowden.com>.

Every change pushed to the `master` branch is built and published by GitHub Pages automatically, usually within a minute or two.

## Writing a blog post

The quickest way is in the browser:

1. Open the `_posts` folder on GitHub and choose **Add file > Create new file**.
2. Name it `YYYY-MM-DD-short-title.md`, for example `2027-01-15-earnings-call-audio.md`. The date in the name is the publication date.
3. Copy in the contents of `_drafts/post-template.md`, change the title and description, and write the post in Markdown.
4. Commit the file. The post appears on the blog and in the RSS feed once the site rebuilds.

To keep a post unpublished while you work on it, save it in `_drafts` instead (no date needed in the name), then move it to `_posts` when it is ready.

Images go in the `images` folder and are referenced as `/images/file-name.jpg`.

Press `.` on any GitHub repository page to open the whole site in a browser-based editor, which is handy for longer edits.

## Updating content

Most of the lists on the site come from data files in `_data`, so updating them means editing a short YAML entry rather than HTML:

| What | File |
| --- | --- |
| Publications, white papers, media | `_data/publications.yml` |
| Funded research projects | `_data/projects.yml` |
| Talks and events | `_data/talks.yml` |
| Menu | `_data/navigation.yml` |

Each file has a comment at the top explaining the fields. Copy an existing entry, paste it in the right place and edit it. Indentation matters in YAML, so keep it aligned with the entries around it. Setting `featured: true` on a journal article shows it on the home page.

Prose pages are plain HTML files in the root folder: `index.html` (home), `research.html`, `teaching.html`, `knowledge-exchange.html` and `publications.html`. Email address, social links and the photo are set once in `_config.yml`.

The design is in `assets/css/style.css`. Colours and fonts are defined as variables at the top of that file.

## Previewing locally (optional)

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Drafts can be previewed with `bundle exec jekyll serve --drafts`.
