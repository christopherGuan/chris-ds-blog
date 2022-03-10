---
toc: true
layout: post
description: A minimal example of using markdown with fastpages.
categories: [markdown]
title: An Example Markdown Post
---
# Example Markdown Post

## Basic setup

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-filename.md`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `filename` is whatever file name you choose, to remind yourself what this post is about. `.md` is the file extension for markdown files.

The first line of the file should start with a single hash character, then a space, then your title. This is how you create a "*level 1 heading*" in markdown. Then you can create level 2, 3, etc headings as you wish but repeating the hash character, such as you see in the line `## File names` above.

## Basic formatting

You can use *italics*, **bold**, `code font text`, and create [links](https://www.markdownguide.org/cheat-sheet/). Here's a footnote [^1]. Here's a horizontal rule:

---

## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![]({{ site.baseurl }}/images/logo.png "fast.ai's logo")

## Code

You can format text and code per usual 

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

Formatting text as shell commands:

```shell
echo "hello world"
./some_script.sh --option "value"
wget https://example.com/cat_photo1.png
```

Formatting text as YAML:

```yaml
key: value
- another_key: "another value"
```


## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |


## Tweetcards

{% twitter https://twitter.com/jakevdp/status/1204765621767901185?s=20 %}


## Footnotes



[^1]: This is the footnote.




## I may be a hypocrite, but I'm not wrong...


# Example Markdown Post

![]({{site.baseurl}}/images/diagram.png "https://github.com/fastai/fastpages")


I've spent over 25 years preaching the value of a portfolio site to artists, software engineers, and designers that wanted to join my studio or learn how to get into games or related industries. Now that I'm 6 months into my PhD and planning for career 2.0, it's past time for me to do the same. This sums up the justification in a single tweet:

<center>{% twitter https://twitter.com/AmeliaMN/status/1021057793753788422?s=20 %}</center>

I recently finished reading [_Build a Career in Data Science_](https://amzn.to/32kxgJg)[^2], which I recommend. It motivated me to start the process of sharing my work.

## Introduction to Fastpages

This site is built with [fastpages](https://github.com/fastai/fastpages), a platform for building static [Jekyll](https://jekyllrb.com/) web blogs from Jupyter Notebooks (JNs). Markdown and Word DOCs are also supported.

![]({{site.baseurl}}/images/diagram.png "https://github.com/fastai/fastpages")

From their github page:

> [fastpages](https://github.com/fastai/fastpages) automates the process of creating blog posts via GitHub Actions, so you don't have to fuss with conversion scripts.  A full list of features can be found on [GitHub](https://github.com/fastai/fastpages).  

Fastpages is built by the [team](https://www.fast.ai/about/) that created the deep learning PyTorch front-end [`fastai`](https://docs.fast.ai) and the Python programming environment [`nbdev`](https://nbdev.fast.ai). The team is led by [Jeremy Howard](https://twitter.com/jeremyphoward), former President and Chief Data Scientist of [Kaggle](https://www.kaggle.com) and author of [_Deep Learning for Coders with Fastai and PyTorch: AI Applications Without a PhD_](https://amzn.to/3p3MpIJ)[^1].

I was first introduced `fastpages` and `nbdev` during the recent [ACM TechTalk](https://learning.acm.org/techtalks), [_It's Time Deep Learning Learned from Software Engineering_](https://webinars.on24.com/acm/howard), presented by Howard and moderated by his collaborator [Hamel Husain](https://twitter.com/hamelhusain).

From [Introducing Fastpages](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html):

> fastpages uses nbdev to power the conversion process of Jupyter Notebooks to blog posts. When you save a notebook into the /_notebooks folder of your repository, GitHub Actions applies nbdev against those notebooks automatically. The same process occurs when you save Word documents or markdown files into the _word or _posts directory, respectively.

Some resources I found helpful in launching this blog:
- The [fastpages github page](https://github.com/fastai/fastpages) has detailed setup instructions
- This [video tutorial](https://youtu.be/L0boq3zqazI) created by [Abdul Majed](https://twitter.com/1littlecoder) walks you through the initial setup process
- A [sample jupyter-based blog page](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html) provides a live demonstration of its capabilities

I was able to get the initial site live quite quickly with little drama, and have found the process of modifying existing content and publishing new material straightforward so far. Before choosing `fastpages` I considered the following hosting / authoring options:

- A general purpose site like [Wix](https://www.wix.com)
- A page on [Medium](https://medium.com) or [Substack](https://substack.com)
- Other JN-based tools like [Pelican](https://docs.getpelican.com/en/latest/index.html)
- Finding a way to use JNs in [blogdown](https://github.com/rstudio/blogdown)[^3]

I decided that Fastpages was the best way for me to publish JN-based work directly, with professional look and feel, on a site that I control, for free. That's a pretty great combination. I also like that it supports Markdown (like this page), is part of the larger fast.ai family of products (and philosophy), and is hosted on github.

Finally, if you still need to be convinced of the value of building a portfolio, and what to include in one give the following resources a look:

- [Advice to aspiring data scientists: start a blog](http://varianceexplained.org/r/start-blog/) on [David Robinson's](https://twitter.com/drob) Variance Explained
- [Data Science Portfolios That Will Get You the Job](https://www.dataquest.io/blog/build-a-data-science-portfolio/)
- [Thinking of blogging about Data Science? Here are some tips and possible benefits.](https://towardsdatascience.com/thinking-of-blogging-about-data-science-here-are-some-tips-and-possible-benefits-680ff0e51d67)

Many of us need to spend less time consuming, and more time creating. Now you know how and why, so go publish something!

---

[^1]: Howard, Jeremy, and Sylvain Gugger. Deep Learning for Coders with Fastai and PyTorch. O’Reilly Media, Inc., 2020.
[^2]: Robinson, Emily, and Jacqueline Nolis. Build a Career in Data Science. Simon and Schuster, 2020.
[^3]: There is a lot of cool stuff going on in R these days and blogdown supports a lot of interesting publishing workflows, but I ultimately decided that it would probably be easier to find a way to publish my R work using fastpages than to publish my Python work with blogdown. Time will tell...


