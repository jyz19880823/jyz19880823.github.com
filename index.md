---
layout: page
title: For Fun!
tagline: Less is More
---
{% include JB/setup %}

This is Emerson from Shanghai. I have a repo just called [aa](https://github.com/jyz19880823/aa) 


## First time with Jekyll

I do not know what to write here. just a gist.

    require "nokogiri"
    require "spidr"
    require "open-uri"
    def yue
      Spidr.site("http://www.somedomain.com") do |spider|
        spider.every_html_page  do |page|
          name = page.title
          doc = Nokogiri::HTML(page.body)
              doc.css(".left_content2").each do |a|
                contents = a.content
                Post.create(:name=>name,:content=>contents)
              end
        end
      end
    end

this is a spider to collect something from the web.
    
    abs

###Posts List

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## To-Do

This theme is still unfinished. If you'd like to be added as a contributor, [please fork](http://github.com/plusjade/jekyll-bootstrap)!
We need to clean up the themes, make theme usage guides with theme-specific markup examples.


