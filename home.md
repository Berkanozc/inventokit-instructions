author: Marc DiPasquale
summary: Create a CodeLab Using Markdown
id: codelab-4-codelab-markdown
categories: codelab,markdown
environments: Web
status: Published
feedback link: https://github.com/Mrc0113/codelab-4-codelab

# CodeLab to Create a CodeLab

## CodeLab Overview
Duration: 0:02:00

Are you trying to create easy to use, visually appealing content for the tech community? This CodeLab will show you how to quickly create your own Google CodeLab just like the one you're using right now. 
When creating a Codelab you have two authoring options: 
1. Using a Google Doc
1. Using a markdown file

In this codelab we are going to use the second option and author our codelab using a markdown file. This gives us the flexibility of using our markdown file for other things and also storing it in our github repo with any code that might be used for a tutorial. 

Here is an example image of another CodeLab that I created:


**Resources:** 
* This codelab's original home is located here: [Link to Codelab](https://www.marcd.dev/codelab-4-codelab)
* The markdown for the original codelab is located here: [codelab.md](https://github.com/Mrc0113/codelab-4-codelab/blob/master/codelab.md)
* [Google CodeLabs Tools Github](https://github.com/googlecodelabs/tools) - The repo that contains the claat tool we'll be using today
* [Google Group for CodeLab Authors](https://groups.google.com/forum/#!forum/codelab-authors) - great forum for asking questions about codelabs and discussing future functionality
* [A blog that I used when getting started with Google Codelabs](https://medium.com/@mariopce/tutorial-how-to-make-tutorials-using-google-code-labs-gangdam-style-d62b35476816)

## Environment Setup
Duration: 0:04:00

In order to create a CodeLab you need *Go* and *claat* (the codelabs command line tool) installed.

The instructions below are what worked for me on Mac, but you can also find instructions [here](https://github.com/googlecodelabs/tools/tree/master/claat) 

#### Install Go 

Install [Go](https://golang.org/dl/) if you don't have it.
You can use Homebrew if you have it on mac 
``` bash
$ brew install go
```

#### Setup Go Environment Variables
Below is what I set on mac, but instructions are [here](https://golang.org/doc/install) for other OS options

``` bash
$ export GOPATH=$HOME/Go
$ export GOROOT=/usr/local/opt/go/libexec
$ export PATH=$PATH:$GOPATH/bin
$ export PATH=$PATH:$GOROOT/bin
```

#### Install claat
Install claat
``` bash
$ go get -u -v -x github.com/googlecodelabs/tools/claat
```

You should now have the *claat* command available to you. 
``` bash
$ claat
```

## Create your initial CodeLab
Duration: 0:05:00

Now that we have the environment setup let's go ahead and create a markdown file where we'll create the actual codelab. 

Negative
: If you're using Windows make sure to set your text editor to use UNIX line endings! 

####
``` bash
$ vim codelab.md
```

#### Fill-in the header metadata
Copy and paste the headers below into your markdown file and change the values appropriately. 
Guidelines are available below the sample headers. 

``` bash
author: Author Name
summary: Summary of your codelab that is human readable
id: unique-codelab-identifier
categories: codelab,markdown
environments: Web
status: Published
feedback link: A link where users can go to provide feedback (Maybe the git repo)
analytics account: Google Analytics ID
```

Metadata consists of key-value pairs of the form "key: value". Keys cannot
contain colons, and separate metadata fields must be separated by blank lines.
At present, values must all be on one line. All metadata must come before the
title. Any arbitrary keys and values may be used; however, only the following
will be understood by the renderer:

* Summary: A human-readable summary of the codelab. Defaults to blank.
* Id: An identifier composed of lowercase letters ideally describing the
  content of the codelab. This field should be unique among
  codelabs.
* Categories: A comma-separated list of the topics the codelab covers.
* Environments: A list of environments the codelab should be discoverable in.
  Codelabs marked "Web" will be visible at the codelabs index. Codelabs marked
  "Kiosk" will only be available at codelabs kiosks, which have special
  equipment attached.
* Status: The publication status of the codelab. Valid values are:
  - Draft: Codelab is not finished.
  - Published: Codelab is finished and visible.
  - Deprecated: Codelab is considered stale and should not be widely advertised.
  - Hidden: Codelab is not shown in index.
* Feedback Link: A link to send users to if they wish to leave feedback on the
  codelab.
* Analytics Account: A Google Analytics ID to include with all codelab pages.

#### Add the Title
Next add your title using a single '#' character
```
# Title of codelab
```

#### Add Sections and Durations
Then for each section use Header 2 or '##' and specify an optional duration beneath for time remaining calculations
Optional section times will be used to automatically total and remaining tutorial times
In markdown I've found that the time is formatted hh:mm:ss

Example
``` bash
## Section 1
Duration: 0:10:00

## Section 2
Duration: 0:05:00
```

#### Add Section Content
Now that we have 2 sections to our titled codelab let's go ahead and add some content to each section. 
Make up your own or copy and paste the example below: 

Copy into section 1 (Below Duration and above Section 2):
```
### Info Boxes
Plain Text followed by green and yellow info boxes 

Negative
: This will appear in a yellow info box.

Positive
: This will appear in a green info box.

You created info boxes!