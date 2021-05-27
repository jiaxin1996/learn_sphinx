sphinx_github_learn
====================

the ide i used
--------------

tried the pycharm, not siut for rST code, because 
it cant give the proview of this kind of langurage.
one can turn to the vscode and download the plugin 
called --> reStructuredText

installed the plugin, u will get error when pewview 
the code.

change the python interpretor like this:

    command + p  

    >python:Selected interpretor

choice a python version > 3

get more detials there: https://zhuanlan.zhihu.com/p/97214287

sphinx_config
--------------

install the sphinx

    .. code-block:: sh 

        $ pip3 install sphinx sphinx_rtd_theme recommonmark

        $ sphinx-quickstart

answer some questions and will get a work folder like this

    .. code-block:: python

        .
        ├── LICENSE
        ├── Makefile
        ├── README.md
        ├── make.bat
        └── source
            ├── _static
            ├── _templates
            ├── conf.py
            └── index.rst
            
then configure the conf.py

    .. code-block:: python

        extensions = [
            'recommonmark',
        ]   

        html_theme = 'sphinx_rtd_theme'

        # The master toctree document.
        master_doc = 'index'

then write a requirments.txt file

    .. code-block:: python

        # markdown suport
        recommonmark
        
        # crate-docs-theme
        sphinx-rtd-theme

one can get the html by using the command: make html. then check it from the 
'build/index.html'

found more details :https://zhuanlan.zhihu.com/p/112215419

github push 3 steps
---------------------

use the command:

    .. code-block:: sh

        $ git add *
        $ git commit -m 'describe'
        $ git push origin master

github cotributor
-------------------

A is the main orgnization of the project and B is a contrabutor.

B have the same right for reading and writing in the project. 

a big right means big responsibility.
So B should do :

    .. code-block:: python

            #fork the code from A and git clone into the local

            $ git checkout -b new_branch    # build a new branch

            edit the files

            $ git push origin new_branch

            compare & pull request

to prevent the polluting of the master branch. learn more at: https://blog.csdn.net/qq_41230365/article/details/86766005