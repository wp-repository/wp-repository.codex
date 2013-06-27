# WP development @GitHub

* __[Repositories](#repositories)__
	* [Branches](#branches)
	* [Tags](#tags)
	* [Readme](#readme)
* __[Release process](#release-process)__
	1. [Checks](#checks)
	2. [Versioning](#versioning)
	3. [Tagging](#tagging)
	4. [Push to SVN](#push-to-svn)
	5. [Re-Versioning](#re-versioning)
* __[WP-Repository Service](#wp-repository-service)__

## Repositories

### Branches
* `master` - main development branch
* `assets` - independent branch for assets to be pushed to WP.org SVN assets folder
* `feature-<feature-name>` - use the power of Git and work on new features in seperate branches

### Tags
* naming conditions: __1.1.1__ (just the version number)
* tag comment: __DO NOT__ use the version number in the comment - it can create problems with SVN sync; 
choose something simple like "release", not a list of changes -> changelog is in the readme

### Readme
*   __README.md__
	> Readme for the GitHub website - [Sample README.md](sample.README.md)

	> Style this page using [GitHub Flavored Markdown (GFM)](https://help.github.com/articles/github-flavored-markdown)

*	__readme.txt__
	> Readme for the WordPress.org repository

	> This file contains the content of the plugin page at wordpress.org and controls certain parameters of the SVN
  
	> [More info](../wp.org-repo#readmetxt)


## Release process

### Checks
* Check if current code base passed the build process - if you use unit testing
* Are all new points in the changelog
* Did you update your language files?
* more?

### Versioning
* Set all version number in all the relevant places for the upcoming tag/release
	* README.md: `Current stable release:` __1.1.1__
	* readme.txt: `Stable tag:` __1.1.1__
	* _plugin-name_.php: `Version:` __1.1.1__

### Tagging [see above](#tags)

### Push to SVN
* push the files of the tag to `SVN/tag/1.1.1/`
* push the readme.txt to `SVN/trunk/`

### Re-Versioning
* Set all version number in all the relevant places for the next tag/release
	* README.md: `Current dev version:` __1.1.2-dev__
	* readme.txt: `Stable tag:` __1.1.1__
	* _plugin-name_.php: `Version:` __1.1.2-dev__


## WP-Repository Service
> [Coming Soon...](http://wp-repository.org)
* 