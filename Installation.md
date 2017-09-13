# Software Installation

## If you already have Python set up

If you have Python set up and installed in a way that you are happy with, you'll just need to make sure you have an up-to-date Astropy and Photutils.  The easiest way to do this is simply: 

	pip install --upgrade astropy
    pip install --no-deps --upgrade git+https://github.com/astropy/photutils.git#egg=photutils
    pip install imexam  # optional

Which should automatically download up-to-date versions of both.

Note that you will also need Jupyter installed to use the notebooks.  If you do not have it, you should be able to do:

    pip install jupyter


## If you don't have Python already

The simplest way to do this is to first download the Anaconda Python Distribution from https://www.continuum.io/downloads , and install that.  Once you've got that working, all you should need to do is this:

  pip install git+https://github.com/astropy/photutils.git#egg=photutils
  pip install imexam  # optional

And that should get you what you need.

If you have trouble with this, you might also look at  the instructions from the last JWST user training workshop: https://github.com/spacetelescope/aas229_workshop/blob/master/Installation_and_Setup.md .  That will get you everything you need (and more!)  A copy of those instructions is included here as "JWSTUT_install.md"
