# HathiTrust Research Center (HTRC)

The [HathiTrust Digital Library](https://www.hathitrust.org/) contains over 14 million volumes scanned from academic libraries around the world (primarily in North America). The [HathiTrust Research Center](https://analytics.hathitrust.org/) allows researchers to access almost all of those texts in a few different modes for computational text analysis. 

This notebook will walk us through getting set-up to analyze [HTRC Extracted Features](https://wiki.htrc.illinois.edu/display/COM/Extracted+Features+Dataset) for volumes in HathiTrust in a Jupyter/Python environment. *Extracted Features* are currently (as of April 2017) the most robust way to access in-copyright works from the HT Library for computational analysis. 

For more information on HTRC: 
* [Library text mining guide page on HTRC](http://guides.lib.berkeley.edu/c.php?g=491766&p=3381443)
* [Programming Historian's Text Mining in Python through the HTRC Feature Reader](http://programminghistorian.org/lessons/text-mining-with-extracted-features)

## Installation

To start we'll need to install a few things:
* Install the *HTRC FeatureReader* to work with Extracted Features using conda:
```
conda install -c htrc htrc-feature-reader
``` 
Or using pip:
```
pip install htrc-feature-reader
pip install matplotlib jupyter
```
* Install Rsync to download Extracted Features from HathiTrust:

  * For linux:
```
yum -y install rsync
```
  * For mac:
```
brew tap homebrew/dupes
brew install rsync
```
