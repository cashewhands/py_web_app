# Using Conda Environment

1. Display Conda environment (to show information about current Conda install)


    (base)username ~ % conda info 

2. List all existing environments


    (base)username ~ % conda env list

3. Create a new environment


    (base)username ~ % conda create -n test_env python=3.8

4. Activate a new environment


    (base) username ~ % conda activate project-env
    (project-env) username ~ %

The (project-env) indicates the current active environment.

you can use conda list to display all packages in this environment.

conda list also supports revision history.

    (project-env) username ~ % conda list --revision

Revision history allows you to rollback your environment to the previous version just like that

    (project-env) username ~ % conda install --revision 1

5. Deactivate/Change your active environment
You can always use conda activate or conda deactivate to switch between your environments. 
You can directly activate the environment you wish to use by using conda activate.


    (project-env) username ~ % conda activate base

    (base) username ~ %

conda deactivate will deactivate your current active environment and
change to the default environment which is the base environment.

    (project-env) username ~ % conda deactivate
    (base) username ~ %

6. Remove the environment
While you are done with this environment and wish to remove it.
You can use conda env remove to remove the environment.


    (base) username ~ % conda env list

Same thing as create, you have to specify the name of the environment you wish 
to remove by using --name.

    (base) username ~ % conda env remove --name project-env

# Uninstall anaconda on Ubuntu
## First of all, you have to install the package anaconda-clean by running the following command:

    conda install anaconda-clean

## Next step is to clean all anaconda related files and directories with the tool we just installed (anaconda-clean):

    anaconda-clean --yes

## Also removes the entire anaconda directory as shown below:

    rm -rf ~/anaconda3

## NOTE: anaconda-clean tool creates a backup of files/dirs after removing the anaconda files, so remove it with the following command:

    rm -rf ~/.anaconda_backup

