# Managing Conda and Anaconda


``conda info``             Verify conda is installed, check version 

``conda update conda``     Update conda package and environment manager

``conda update anaconda``  Update the anaconda meta package


# Managing Environments

``conda info --envs``                               Get a list of all my environments
``conda info -e``                                   Activate environment shown with *

``conda create --name snowflakes biopython``        Create an environment and install program(s)
``conda create -n snowflakes biopython``            



``conda activate snowflakes``                       Activate the new environment to use it



``conda deactivate``                                Deactivate the environment

``conda create -n bunnies python=3.4 astroid``      Create a new environment, specify Python version

``conda create -n flowers --clone snowflakes``      Make exact copy of an environment

``conda remove -n flowers --all``                   Delete an environment

``conda env export > puppies.yml``                  Save current environment to a file

``conda env create -f puppies.yml``                 Load environment from a file

# Managing Python
``conda search --full-name python``                 Check versions of Python available to install
``conda search -f python``



``conda create -n snakes python=3.4``               Install different version of Python in new environment

# Managing .condarc Configuration

``condaconfig --get``                               Get all keys and values from my .condarc file

``condaconfig --get channels``                      Get value of the key channels from .condarc file

``condaconfig --add channels pandas``               Add a new value to channels so ``condalooks for packages in this location

# Managing Packages, Including Python
``condalist``                                       View list of packages and versions installed in active environment

``condasearch beautiful-soup``                      Search for a package to see if it is available to ``condainstall

``condainstall -n bunnies beautiful-soup``          Install a new package

NOTE: If you do not include the name of the environment, it will install in the current active environment.

``condaupdate beautiful-soup``                      Update a package in the current environment

``condasearch --override-channels -c pandas bottleneck``    Search for a package in a specific location (the pandas channel on Anaconda.org)

``condainstall -c pandas bottleneck``               Install a package from a specific channel

``condasearch --override-channels -c defaults beautiful-soup``  Search for a package to see if it is available from the Anacondarepository

``condainstall iopro accelerate``                   Install commercial Continuum packages

``condaskeleton pypi pyinstrument``                 Build a condapackage from a Python Package Index (PyPi) Package
``condabuild pyinstrument``



# Removing Packages or Environments


``condaremove --name bunnies beautiful-soup``           Remove one package from any named environment

``condaremove beautiful-soup``                          Remove one package from the active environment

``condaremove --name bunnies beautiful-soup astroid``   Remove multiple packages from any environment

``condaremove --name snakes --all``                     Remove an environment

