# HathiTrust Research Center (HTRC)

The [HathiTrust Digital Library](https://www.hathitrust.org/) contains over 14 million volumes scanned from academic libraries around the world (primarily in North America). The [HathiTrust Research Center](https://analytics.hathitrust.org/) allows researchers to access almost all of those texts in a few different modes for computational text analysis. 

This notebook will walk us through getting set-up to analyze [HTRC Extracted Features](https://wiki.htrc.illinois.edu/display/COM/Extracted+Features+Dataset) for volumes in HathiTrust in a Jupyter/Python environment. *Extracted Features* are currently (as of April 2017) the most robust way to access in-copyright works from the HT Library for computational analysis. 

For more information on HTRC: 
* [Library text mining guide page on HTRC](http://guides.lib.berkeley.edu/c.php?g=491766&p=3381443)
* [Programming Historian's Text Mining in Python through the HTRC Feature Reader](http://programminghistorian.org/lessons/text-mining-with-extracted-features)

## Installation

To start we'll need to install a few things:
* Install the *HTRC Feature Reader* to work with Extracted Features: 
```
conda install -c htrc htrc-feature-reader
``` 
or
```
pip install htrc-feature-reader
pip install matplotlib jupyter
```
* Install Rsync to download Extracted Features from HathiTrust:

  * For Linux:
```
yum -y install rsync
```
  * For Mac you need to use [Homebrew](https://brew.sh/) to install Rsync. To install Homebrew:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
  * And then to install Rsync on Mac using Homebrew:
```
brew tap homebrew/dupes
brew install rsync
```

## Add volumes from HTRC

### Finding Volume IDs in HathiTrust

To build your own corpus, you will need to find the volume ID for each volume you'd like to include from the [HathiTrust Library](https://www.hathitrust.org/).

* Search for your book, and copy the URL from the *Limited (Search Only)* or *Full View* links under the work. <img src="files/judith-butler-ht.png">
* The final string of characters after the final / is your volume ID
* For example, mdp.39015070698322 is the volume ID for "https://hdl.handle.net/2027/mdp.39015070698322"


