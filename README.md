# resume-builder
Resume-Builder is a simple, Jekyll-based resume that can be hosted using GitHub
pages or any web service that can serve static files.

The purpose of this template is to serve as a flexible starting point so that an individual may customize to fit their own needs and experiences.

## Installation
To install Jekyll and it's dependencies you will need Ruby installed on your machine.  If you have a Windows machine there are several services to do this for you.

```
# Install the Jekyll Ruby Gem
gem install jekyll

# Clone the base git repo
git clone https://github.com/austin94/resume-builder
```

For full installation instructions for Jekyll refer to their documentation
[http://jekyllrb.com/docs/installation](http://jekyllrb.com/docs/installation/)

## Serving Files
Jekyll is a static site generator.  This allows us to create reusable components and use data structures, like JSON, to
help us organize data and then create static HTML files to host separately.

Jekyll has a built-in utility that watches for file changes and re-compiles your assets automatically.  You can start this
utility with:

```
# Change to repo directory
cd resume-builder

# Watch for Jekyll changes
jekyll serve
```

This makes your site visible at [localhost:4000](http://localhost:4000).  You static files can be found under the *_site*
directory.  This is what you will host later on.

## Basic Data Structures
The data that the resume uses can be found in the *_data/information.json* file.  This file determines the sections of your resume and the experiences included.  My examples are:

*   Education
*   Work Experience
*   Community Service

### Sample Structure
```
{
  "name": "Education",
  "experiences": [
    {
      "name": "Kansas State University",
      "url": "http://www.k-state.edu",
      "location": "Manhattan, KS",
      "subText": "Senior with a 3.60 cumulative GPA. Graduating in Spring 2016.",
      "description": "",
      "involvement": [
        {
          "description": "Graduated with a degree in Computer Science - Software Engineering with a minor in Business."
        },
        {
          "description": "Focus in scalable web and mobile technologies."
        },
        {
          "description": "Vice-President, RLC Chairman, Homecoming, and Recruitment Chairman of the Kansas State Chapter of the Delta Chi Fraternity."
        },
        {
          "description": "1st place in the CIS Department and 2nd overall in Engineering for developing a web-based responsive recruitment display for the Spring 2014 Engineering Open House."
        }
      ]
    }
  ]
}
```

As you change the JSON structure the *jekyll serve* command from earlier will recognize a file change and recompile your static files.  Refresh the page to view changes.

## Image Thumbnail, Name, and Description
To change the name and footer of the resume, update the **_config.yml** file.

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
### Github
To deploy as a github page:

* Fork this repository
* Rename it to <github_username>.github.io
* Wait 15 minutes for your resume to be shown

To push changes follow the steps above and push your changes to your repo and the changes should be visible in a few minutes (if not instantly).

### Anywhere else
You can find the static files created under the *_site* directory.  These files can be hosted as is.
