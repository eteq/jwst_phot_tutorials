This will be an interactive workshop so be sure to come with a laptop prepared to try out some of the tools that will be discussed and demonstrated.

### If you installed weeks ago, several of the packages have updated releases. 

You can update all the software in your environment using:
    
    % conda update --yes --all
    
You can also update individual packages with conda update, these are the two packes with new versions:

    % conda update -c http://ssb.stsci.edu/astroconda stginga
    % conda update -c http://ssb.stsci.edu/astroconda imexam

If you have any problem with the instructions here, please open an issue at https://github.com/spacetelescope/aas229_workshop/issues/

# 1. Clone This Repository

First, download this repository by either doing:

    % git clone http://github.com/spacetelescope/aas229_workshop.git

or by downloading and then expanding the repository file.

Then, cd into the aas229_workshop directory.

# 2. Install Anaconda, AstroConda

Note: please do this ahead of the workshop if possible.

## 2a. Getting Anaconda Anaconda

### Mac, Linux

If you don't already have Anaconda installed, install the the Anaconda distribution for Python 3.5, which we have packaged along with some additional software. Downloads for Mac and Linux can be found at:

    http://ssb.stsci.edu/conda/installers/AstroConda-1.0.2-Linux-x86_64.sh
    http://ssb.stsci.edu/conda/installers/AstroConda-1.0.2-MacOSX-x86_64.sh

These shell installers include both Anaconda and the AstroConda software repository, which contains additional tools that will be shown at the workshop. To run the installer, cd to where you downloaded it to, and choose the appropriate command from below:

    % ./AstroConda-1.0.2-Linux-x86_64.sh
    % ./AstroConda-1.0.2-MacOSX-x86_64.sh

If you have trouble installing using the above files, you will need to download Anaconda separately (https://www.continuum.io/downloads). Then, proceed to Step 2b. If the installer above somehow did not install the versions needed, also go to Step 2b.

More information about AstroConda can be found at http://astroconda.readthedocs.io/en/latest/ (currently does not support Windows build).

### Windows

You will need to download Anaconda separately (https://www.continuum.io/downloads). Then, proceed to Step 2b.

## 2b. Create an  Anaconda environment for the workshop

If you have Anaconda already installed you can skip 2a and go straight on to this step.

Note: You need to be inside the aas229_workshop directory for this to work.

The command below will create an environment called "aas229-workshop", but you can change that to any other desirable name by replacing the quoted name.

### Mac, Linux

You can create a special environment for this workshop which contains all the software you will need using the environment file below:

    % conda config --add channels http://ssb.stsci.edu/astroconda
    % conda env create -n aas229-workshop --file environment.yml
    % source activate aas229-workshop

### Windows

You can create a special environment for this workshop which contains most of the software you will need using the environment file below:

    % conda config --add channels http://ssb.stsci.edu/astroconda
    % conda env create -n aas229-workshop --file environment_win.yml
    % activate aas229-workshop

Then, you can install the rest of the packages using:

    % pip install -r pip_requirements_win.txt

Note: Windows distribution currently does not yet support imexam.

# 3. Check Installation

Note: You need to be inside the aas229_workshop directory for this to work.

You can run the check_env.py script to perform a basic check of your Python environment and some of the required dependencies:

    % python check_env.py

# 4. Pick Up Changes

To pick up any updates for workshop materials, make sure you are in the aas229_workshop directory and then use the following command:

    % git pull

This *may* result in an error, if you've modified any of the files that have changed since you last pulled from git.  In that case, you'll need to do:

    % git fetch origin master
    % git reset --hard origin/master

NOTE: This will overwrite any notebooks you've modified.  Be sure to back up any changes you care about.  Or if you really want to keep something, you can ask one of the instructors to show you how to do a more fine-grained update using advanced git commands.
    
The commands above only work if you used git in Step 1. The rebase command will not work properly if you have modified the materials (e.g., running the notebooks). In that case or if you downloaded the materials manually, you will have to update the changed files manually as well; e.g., by downloading the updated file (the RAW format) via GitHub web interface.

Software covered in this workshop should not need any more updates after Steps 2 and 3. However, in the event of any necessary quick fix, instructions will be given out during the workshop (e.g., using conda or pip commands).