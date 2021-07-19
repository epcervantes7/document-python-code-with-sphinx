# document-python-code-with-sphinx
autogenerate documentation for python using sphinx


## Install  Sphinx
```console
eve@house:~$ pip install sphinx
```

## Create a directory for documentation

```console
eve@house:~$ mkdir docs
eve@house:~$ cd docs
```

## Use sphinx-quickstart to generate basic configuration in the docs directory

```console
eve@house:~/docs$ sphinx-quickstart
```
you can enter some parameters or use the default values in my case this command shows:

```bat
Welcome to the Sphinx 2.2.1 quickstart utility.
Please enter values for the following settings (just press Enter to
accept a default value, if one is given in brackets).
Selected root path: .
You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]: y
The project name will occur in several places in the built documentation.
> Project name: My project
> Author name(s): My name
> Project release []: 0.1
If the documents are to be written in a language other than English,
you can select a language here by its language code. Sphinx will then
translate text that it generates into that language.
For a list of supported codes, see
https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
> Project language [en]: 
Creating file ./source/conf.py.
Creating file ./source/index.rst.
Creating file ./Makefile.
Creating file ./make.bat.
Finished: An initial directory structure has been created.
You should now populate your master file ./source/index.rst and create other documentation
source files. Use the Makefile to build the docs, like so:
   make builder
where "builder" is one of the supported builders, e.g. html, latex or linkcheck.
```
As result a set of files and directories were created:

```console
eve@house:~/docs$ ls
build  make.bat  Makefile  source
```

## autogenerate .rst files
```console
eve@house:~/docs$ sphinx-apidoc -o source/ ../<code package>
 ```
 
 ## Build
```console
eve@house:~/docs$ sphinx-build -b html source/ build/
 ```
 
 And... ready ... your documentation is in the build directory
 

 
