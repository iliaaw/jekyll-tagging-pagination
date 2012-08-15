jekyll-tagging-pagination
=========================

Plugin for [Jekyll](http://github.com/mojombo/jekyll) static site generator, to enable pagination of posts organized by tags.

Though Jekyll provides pagination, it is only available in index pages. jekyll-tagging-pagination makes pagination also available in tag pages.

Installation
------------
Copy `tags-pagination.rb` file into `_plugins` directory (you might need to create it before).

Usage
-----

In your post's YAML front matter, add tags like this:

    tags:
    - jekyll
    - pagination

In your `_layouts` directory, create file `tag.html`. That template is used to create an index page for every tag mentioned in posts. Inside that template, use `paginator` object like this:

    {% for post in paginator.post %}
        {{ post.title }}
    {% endfor %}

`paginator` object provides tag information, use `pagination.tag` for that.