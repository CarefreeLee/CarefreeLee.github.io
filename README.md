## Repository information
This repository is a fork of [Carte](https://github.com/Wiredcraft/carte) which is a simple Jekyll based documentation website for APIs which was designed for people to build their own documentation upon.

## Install

1. Install Ruby
1. Install RubyGems -> Use the install approach at the bottom of this page: https://rubygems.org/pages/download
1. Install Jekyll -> ``gem install jekyll``
1. Clone this repository to your local machine
1. Go to the root of the repository and run ```jekyll serve --watch```
1. Go to http://localhost:4000

## How to...

### Add a new API call

You can add a new API call by simply adding a new post in the `_posts` folder. Jekyll by default forces you to specify a date in the file path: it makes us sad pandas too, but you'll have to stick to this format. You can use dates to control the order in which API calls are displayed in the interface.

Each API call can define a few values in its YAML header:

Variable | Mandatory | Default | Description
--- | --- | --- | ---
``title`` | Y | - | A short description of what that call does.
``path`` | N | - | The URL for the API call, including potential parameters.
``type`` | N | - | Set it to `PUT`, `GET`, `POST`, `DELETE` or nothing (for parts of your documentation that do not relate to an actual API call).

A typical header:

```
---
path: '/stuff/:id'
title: 'Delete a thing'
type: 'DELETE'

layout: nil
---
```

We then describe the request and response (or whatever else you wish to talk about) in the body of our post. Check the placeholders present in the `_posts` folder to get an idea of what it can look like.

### Group calls

Adding a category to your YAML header will allows you to group methods in the navigation. It is particularly helpful as you start having a lot of methods and need to organize them. For example:

```
---
category: Stuff
path: '/stuff/:id'
title: 'Delete a thing'
type: 'DELETE'

layout: nil
---
```

### Order calls

As mentioned earlier, Jekyll orders the call posts by date. Therefore I suggest to just use the dates' year field as ordering numbers.

For special posts that should always be shown at the top of the list, you could set the file name to ``9999-01-01-file-name-here.md``.    
Regular call posts could ``0001-01-01-file-name-here.md`` and be incremented from there to ``0002-01-01-file-name-here.md`` etc.

### Edit the design

The default UI is mostly described through the `css/style.css` file and a couple short jQuery scripts in the `/_layouts/default.html` layout. Hack it to oblivion.
