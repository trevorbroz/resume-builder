# resume-builder
A Jekyll site for easy resume building.

## Introduction
There are many different ways to create a resume.  A simple word document, a PDF, and LinkedIn are all good examples,
but many employers and recruiters are looking for individuals that go above and beyond the normal avenues.  Many times
an online resume can help give you that extra step to get the interview or that first call.  I've created a simple 
[Jekyll](https://jekyllrb.com/) site that will allow anyone to easily create and customize their own online resume.

To get started you can download the base template here: [https://github.com/austin94](https://github.com/austin94)

## Installation
To install Jekyll and it's dependencies you will need Ruby installed on your machine.  If you have a Windows machine
there are several services to do this for you.

```
# Install the Jekyll Ruby Gem
gem install jekyll

# Clone the base git repo
git clone https://github.com/alskdfads.git
```

For full installation instructions for Jekyll refer to their documentation 
[http://jekyllrb.com/docs/installation](http://jekyllrb.com/docs/installation/)

## Serving Files
Jekyll is a static site generator.  This allows us to create reusable components and use data structures, like JSON, to
help us organize data and then create static HTML files to host separately.

Jekyll has a built-in utility that watches for file changes and re-compiles your assets automatically.  You can start this
utility with:

```
jekyll serve
```

This makes your site visible at [localhost:4000](http://localhost:4000).  You static files can be found under the *_site* 
directory.  This is what you will host later on.

## Basic Data Structures
The data that the resume uses is divided into three categories:

*   Education
*   Community Service
*   Work Experience

These can be found in the JSON files under the *_data* directory.

### Education
```
  {
    "name": "Kansas State University",
    "url": "http://www.k-state.edu",
    "location": "Manhattan, KS",
    "subText": "Senior with a 3.60 cumulative GPA. Graduating in Spring 2016.",
    "involvement": [
      {
        "description": "Graduating with a degree in Computer Science - Software Engineering."
      },
      {
        "description": "Sample description 1"
      },
      {
        "description": "Sample description 2"
      }
    ]
  }
```

The JSON files determine what data is used to render the static resume page.  The *jekyll serve* command from earlier
will recognize changes in your files and recompile the page.  Just refresh to view the changes.

### Other categories
The other categories act similar to education in style and content.  The template automatically handles missing 
information.

## Image Thumbnail, Name, and Description
To change the name and description of the resume, update the **_config.yml** file.

```
  title: Austin Green
  email: austingreenkansas@gmail.com
  description: >
    I am currently a Senior at Kansas State University.  I will be graduation in the Spring of 2016 with a
    Bachelors of Engineering in Software Engineering with a minor in Business.  I enjoy finding unique
    solutions to common problems with an emphasis on scalable web and mobile.
  baseurl: ""
  url: http://austingreen.info
  github_username:  austin94
```

To replace the image thumbnail with your own, overwrite the **profile.png** image in the *images* directory.

## Deployment
ToDo
