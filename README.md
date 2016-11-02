# Asciidoc template for Red Hat Public Sector Workshops

### Usage

Install `ascii_binder`. 

	http://www.asciibinder.org/latest/guides/user_guide.html

Asciidoc Refrence Guide:

	http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/


Use git to track your changes. 

```
$ cd Containers_Workshop_Site
$ git add .
$ git commit -m "Initial commit on docs repo"
```

Add a new folder to the repo full of the new `adoc`s you are commiting. 

```
mkdir resources
cd resources
touch newfile.adoc
```

Then add the folder and file structure to the `_topicmap.yml`

```
---
Name: Resources
Dir: resources
Topics:
  - Name: Resource
    File: newfile
```

Then build it with `asciibinder`. This will build a website with html, css, and js in `_preview`. From here you can take that folder and deploy it to a webserver of your choice.

```
$ asciibinder
```

Then in `_preview/red-hat-public-sector/latest`, you will be able to copy the `latest` folder to a S3 bucket and enable static website hosting.  

<TO DO> S3 Bucket hosting how to.