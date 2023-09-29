---
layout: page
title: Setup
---

## In a Data Carpentry Workshop  
This workshop is designed to be run on pre-imaged Amazon Web Services (AWS)
instances (a computer with all the required programs and files to which you will have access from your computer). 
Except for a spreadsheet program and an internet browser, all of the command 
line software and data used in the workshop are hosted on an Amazon 
Machine Image (AMI). If you are signed up to take 
a Pangenomics Data Carpentry Workshop, **you do not need to worry about setting
up an AMI instance.** The Carpentries staff will create an instance 
for you, which will be provided at no cost. 
This setup is true for both self-organized and centrally-organized workshops. 
Your Instructor will provide instructions for connecting to the AMI instance at the workshop.

If you are in The Carpentries-Workshop, you do not even need to install a bash terminal; the R-studio terminal provided in the AWS-AMI is enough to run all the commands in the lesson. 
Instead of connecting by `ssh`, users can simply use the R-studio AMI terminal. 

This lesson requires a working spreadsheet program. 
If you don't have a spreadsheet program already, you can use LibreOffice. 
It's a free, open-source spreadsheet program.

## Running the lesson by yourself (Not in a Data Carpentry Workshop)

### Required  software  
If you are not in a Data Carpentry Workshop, the software you need is listed in the table below. Follow the instructions in Option A *or* Option B to have access to these programs.  


| Software | Version | Manual | Available for | Description |
| -------- | ------------ | ------ | ------------- | ----------- |
| [Prokka](https://github.com/tseemann/prokka) | 1.14.6 | [GitHub](https://github.com/tseemann/prokka#invoking-prokka) | Linux, MacOC, Windows | Bacterial, archaeal and viral assembly annotation |
|[ncbi-genome-download](https://github.com/kblin/ncbi-genome-download)  | version | [GitHub](https://github.com/kblin/ncbi-genome-download#usage) | Downloading genomes from the NCBI |
|[Anvi'o](https://anvio.org/)| version |[Pangenomics Workflow Manual](https://merenlab.org/2016/11/08/pangenomics-v2/)|Linux & MacOS| *multi-omics* analysis including Pangenomics|
|[GET_HOMOLOGUES](https://github.com/eead-csic-compbio/get_homologues)|version|[GitHuB](http://eead-csic-compbio.github.io/get_homologues/manual/)|Available for| Sequence clustering|
|[PPanGGOLiN](https://github.com/labgem/PPanGGOLiN)|version |[GitHub Wiki](https://github.com/labgem/PPanGGOLiN/wiki)|Available for| Pangenomics |


### Option A: Using the lessons with Amazon Web Services (AWS)

Follow these [instructions on creating an Amazon instance](https://carpentries-incubator.github.io/metagenomics-workshop/AMI-setup/index.html). Use the AMI `ami-0f58e878fa70cc201` named `The Carpentries Lab Metagenomics v1.0` listed on the Community AMIs page. Please note that you must set your location as `N. Virginia` to access this community AMI. You can change your location in the upper right corner of the main AWS menu bar. The cost of using this AMI for a few days, with the t2.medium instance type, is very low (about USD $2.00 per user per day). Data Carpentry has *no* control over AWS pricing structure and provides this cost estimate without guarantees. Please read AWS documentation on pricing for up-to-date information. 

If you're an Instructor or Maintainer or want to contribute to these lessons, please contact us at [team@carpentries.org](mailto:team@carpentries.org), and we will start instances for you. 

In this instance, you can use the terminal available in RStudio, and users won't need
to install their own terminals or use `ssh` (see [Instructor Notes](https://carpentries-incubator.github.io/metagenomics-workshop/guide/index.html)). **If, nevertheless, you
prefer that the users install their own terminals**, directions to install them are included 
for each Windows, Mac OS X, and Linux below in the Option B section. For Windows, you will need to install Git Bash, PuTTY, or the Ubuntu Subsystem.

### Option B: Following the lessons on your local machine  
If you trust that your computer is powerful enough and want to have all the programs installed, you can follow all the workshops without using an
AWS remote machine. To do this, you will need to install all of the software used in the workshop and obtain a copy of the
dataset. Instructions for doing this are below.  


#### **Data**   
The data used in this workshop are available on Zenodo. Please read the Zenodo 
page linked below for information about the data and access to the data files. Because this workshop works 
with real data, be aware that file sizes for the data are large.information 
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4285900.svg)](https://doi.org/10.5281/zenodo.4285900)

More information about these data will be presented in the [first episode of the Data processing and visualization for metagenomics lesson](https://carpentries-incubator.github.io/metagenomics/01-background-metadata/index.html).


#### **Install a Bash terminal** 

> ## Windows
> - Download the [Git for Windows installer](https://git-for-windows.github.io/). Run the installer and follow the steps below:
>   + Click on "Next" four times (two times if you've previously installed Git). You don't need to change anything in the information, location, components, and start menu screens.
>   + Select "Use the nano editor by default" and click on "Next".
>   + Keep "Use Git from the Windows Command Prompt" selected and click on "Next". If you forget to do this, the programs that you need for the workshop will not work properly. If this happens, rerun the installer and select the appropriate option.
>   + Select "Use bundled OpenSSH" and click on "Next".
>   + Select "Use the OpenSSL Library" and click "Next".
>   + Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
>   + Select "Use Windows' default console window" and click on "Next".
>   + Select "Default (fast-forward on merge)" and click on "Next".
>   + Select "None" (Do not use a credential helper) and click on "Next".
>   + Select "Enable file system caching" and click on "Next".
>   + Ignore "Configuring experimental options" and click on "Install".
>   + Click on "Install".
>   + Click on "Finish".
>   + If your "HOME" environment variable is not set (or you don't know what this is):
>   + Open command prompt (Open Start Menu, then type `cmd` and press [Enter])
>   + Type the following line into the command prompt window exactly as shown: `setx HOME "%USERPROFILE%"`
>   + Press [Enter], and you should see `SUCCESS: Specified value was saved.`
>   + Quit the command prompt by typing `exit` and then pressing [Enter]
>   + See the [video tutorial](https://youtu.be/yo7Z-BEG62A) for an example of how to install Git on Windows 11.
>   
> - An **alternative option** is to install PuTTY
>  by going to the [the installation page](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html). For most newer computers, click on putty-64bit-X.XX-installer.msi to download the 64-bit version. If you have an older laptop, you may need to get the 32-bit version putty-X.XX-installer.msi. If you aren't sure whether you need the 64 or 32-bit version, you can check your laptop version by following [the instructions here](https://support.microsoft.com/en-us/help/15056/windows-32-64-bit-faq). Once the installer is downloaded, double-click on it, and PuTTY should install.
> - **Another alternative option** is to use the Windows Subsystem Linux (WSL). This option is available for Windows 10 and Windows 11 - detailed [instructions are available here](https://learn.microsoft.com/en-us/windows/wsl/install).
> See the [video tutorial](https://youtu.be/YoNdTuN-YWk) for an example of how to install WSL with Ubuntu 22.04 on Windows 11.
> 
{: .solution}

> ## macOS
> -  The default shell in some versions of macOS is Bash, and Bash is available in all versions, so no need to install anything. You access Bash from the Terminal Application (found in /Applications/Utilities). See how to open the terminal in the [video tutorial](https://www.youtube.com/watch?v=FuNsWg_VzeQ). You may want to keep the terminal in your dock for this workshop.
{: .solution}

> ## Linux
>  - The default shell is usually Bash, and there is usually no need to install anything. To see if your default shell is Bash type, echo $SHELL in a terminal and press the Enter key. If the message printed does not end with `/bash`, then your default is something else, and you can run Bash by typing `bash`.
{: .solution}


#### **Install Miniconda3**

These instructions assume familiarity with the command line and with installation 
in general. There are different operating systems and many different versions
of operating systems and environments, so these may not work on your computer. If an 
installation doesn't work for you, please refer to the user guide for the tool listed in the table above.
If you have difficulties with the installations or find better ways to install things in your operating system, please raise an [Issue](https://github.com/carpentries-incubator/metagenomics/issues) to let us know.

To make a [Conda](https://conda.io/projects/conda/en/latest/index.html) environment, first, you need to install Conda. We recommend installing the [Miniconda3](https://docs.conda.io/en/latest/miniconda.html) version. Miniconda is a package manager that includes Conda and its dependencies and simplifies the installation process. Please first install Miniconda3 (installation instructions below) and then proceed to the installation of the environment.

> ## Linux
> 
> To install miniconda3, see the [video tutorial](https://youtu.be/0PqwShSDH20)
{: .solution}

> ## MacOSX
> In a terminal type:
> ~~~
> $ curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
> $ bash Miniconda3-latest-MacOSX-x86_64.sh
> ~~~
> {: .bash}
> Then, follow the instructions that you are prompted with on the screen to install Miniconda3.
{: .solution}

> ## WSL
> See the video tutorial, [installing Miniconda3 on WSL Ubuntu](https://youtu.be/owQgZoE-GrY)
{: .solution}


#### **Install the metagenomics environment**

Once your Miniconda3 ready, follow these instructions to install and activate the metagenomics environment. 

> ## Linux: Option 1 (recommended)
> The easier way to install the environment is using the [specifications file](https://github.com/carpentries-incubator/metagenomics/blob/gh-pages/files/spec-file-Ubuntu22.txt) 
> for Linux Ubuntu 22.04, which has the exact versions of each tool in this environment. You can use the spec file as follows:  
> ~~~
> $ conda create --name metagenomics --file spec-file-Ubuntu22.txt
> ~~~
> {: .bash}
> More information about how to use environments and spec files is available at [conda documentation](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
{: .solution}

> ## Linux: option 2
> Another way to create an environment is with a `ỳml` file.
> This environment can be modified by adding or deleting tools in a file `metagenomics-Ubuntu22.yml`.
> 
> In Ubuntu 22.04, copy this file [metagenomics-Ubuntu22.yml](https://github.com/carpentries-incubator/metagenomics/blob/gh-pages/files/metagenomics-Ubuntu22.yml) 
> to your computer and follow the instructions in the [video tutorial](https://youtu.be/0Ks1k9gg3E0)
{: .solution}

> ## MacOSX
> It has been difficult to find compatibility between all the dependencies of each package installed in the
> metagenomics environment. In the case of the latest version of macOS (Monterey), the MaxBin2 package can be 
> installed, but it does not fully work at the time of use.
> Copy the file [metagenomics-macOS.yml](https://github.com/carpentries-incubator/metagenomics/blob/gh-pages/files/metagenomics-macOS.yml) in your computer and run: 
> ~~~
> $ conda env create -f metagenomics-macOS.yml
> ~~~
> {: .bash}  
{: .solution}

> ## WSL
> In the case of Windows Subsystem for Linux WSL Ubuntu 22.04, the MaxBin2 package has an incompatibility 
> with the checkm-genome package, so we have decided to leave it out of the metagenomics environment and 
> create its own environment with the file([metagenomics-maxbin.yml](https://github.com/carpentries-incubator/metagenomics/blob/gh-pages/files/metagenomics-maxbin.yml)).
> The file for the metagenomics environment is [metagenomics-WSLUbuntu.yml](https://github.com/carpentries-incubator/metagenomics/blob/gh-pages/files/metagenomics-WSLUbuntu.yml)
> See the [video tutorial](https://youtu.be/kHYmffZYxcI)
> ~~~
> $ conda env create -f metagenomics-maxbin.yml
> $ conda env create -f metagenomics-WSLUbuntu.yml
> ~~~
> {: .bash}  
{: .solution} 


#### **Execute some remaining installation scripts**  

Change `dcuser` with your own username.
And run all these lines:
~~~
bash /home/dcuser/.miniconda3/envs/metagenomics/opt/krona/updateTaxonomy.sh                                
wget ftp://ftp.ncbi.nih.gov/pub/taxonomy/taxdump.tar.gz 
tar -xzf taxdump.tar.gz 
mkdir .taxonkit
cp names.dmp nodes.dmp delnodes.dmp merged.dmp /home/dcuser/.taxonkit
rm *dmp readme.txt taxdump.tar.gz gc.prt 
~~~
{: .bash}  

#### **Install R and RStudio**

R and RStudio are two separate pieces of software:

R is a programming language that is especially powerful for data exploration, visualization, and statistical analysis RStudio is an integrated development environment (IDE) that makes using R easier. In this course, we use RStudio to interact with R.

> ## Mac OS X
> -  Download R from the [CRAN website](https://cran.r-project.org/bin/macosx/).
> + Select the .pkg file for the latest R version
> + Double-click on the downloaded file to install R
> + It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed by some packages)
> + Go to the [RStudio download](https://www.rstudio.com/products/rstudio/download/#download) page
> + Under Installers, select RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit) (where x, y, and z represent version numbers)
> + Double-click the file to install RStudio
> + Once it’s installed, open RStudio to ensure it works and you don’t get any error messages.
{: .solution}

> ## Windows
> -  Download R from the [CRAN website](https://cran.r-project.org/bin/windows/base/release.htm).
> + Run the .exe file that was just downloaded
> + Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
> + Under Installers select RStudio x.yy.zzz - Windows Vista/7/8/10 (where x, y, and z represent version numbers)
> + Double-click the file to install it
> + Once it’s installed, open RStudio to ensure it works and you don’t get any error messages.
{: .solution}

> ## Linux
> - Follow the instructions for your distribution from [CRAN](https://cloud.r-project.org/bin/linux). They provide information to get the most recent version of R for common distributions. For most distributions, you could use your package manager (e.g., for Debian/Ubuntu, run sudo apt-get install r-base, and for Fedora, sudo yum install R). However, we don’t recommend this approach as the versions provided by this are usually out of date. In any case, make sure you have at least R 3.3.1.
> + Go to the [RStudio](https://www.rstudio.com/products/rstudio/download/#download) download page
> + Under Installers, select the version that matches your distribution, and install it with your preferred method (e.g., with Debian/Ubuntu ´sudo dpkg -i rstudio-x.yy.zzz-amd64.deb´ at the terminal).
> + Once it’s installed, open RStudio to ensure it works and you don’t get any error messages.
{: .solution}

#### **Install R libraries**

| Software | Version | Manual | Description |
| -------- | ------------ | ------ | ------------- |
| [phyloseq](https://github.com/joey711/phyloseq) | 1.39.1 | [GitHub](https://github.com/joey711/phyloseq) | Explore, manipulate and analyze microbiome profiles with R |
| [ggplot2](https://ggplot2.tidyverse.org/) | 3.3.6 | [GitHub](https://github.com/tidyverse/ggplot2) | System for declaratively creating graphics, based on The Grammar of Graphics |

Type these commands in your console:
~~~
> install.packages("phyloseq")
> install.packages("ggplot2")
~~~
{: .language-R}

## NCBI-genome-download installaation

There are two ways to install this package. The firts one is with pip. It is recommended to upgrade the pip version to the newest
~~~
pip install --upgrade pip
pip install .
~~~

Then you can install the package 
```
pip install ncbi-genome-download
```
The other installation option is with conda, you can refer to the website (highly recommended).

```
conda install -c bioconda ncbi-genome-download
```


## Prokka installation

# Bioconda
If you use [Conda](https://conda.io/docs/install/quick.html)
you can use the [Bioconda channel](https://bioconda.github.io/):

```
conda install -c conda-forge -c bioconda -c defaults prokka
```
# MacOS

```
sudo cpan Time::Piece XML::Simple Digest::MD5 Bio::Perl
git clone https://github.com/tseemann/prokka.git $HOME/prokka
$HOME/prokka/bin/prokka --setupdb
```
**You can test your installation typing `prokka` and it should display its help screen**


## Installation of Anvi'o

* Install a stable release of anvi’o on a Mac, Linux, or Windows running computer (best option for end users).
* Use anvi’o from the active development branch (best option for developers).
* Run anvi’o through its Docker containers without any installation (best option for the lazy).  


This environment can be modified by adding or deleting tools in a file `pangenomics.yml`, 
original metagenomics.yml file had the following content:  
~~~
$ cat pangenomics.yml
~~~
{: .bash}
~~~
name: pangenomics                                                                
dependencies:                                      
  - ncbi-genome-download 
  - prokka
  - anvio
  - get_homologues
  - pangolin
~~~
{: .output}

Then you can create your own metagenomics conda environment using the metagenomics.yml file.  
~~~
$ conda env create -f pangenomics.yml
~~~
{: .bash}  

## Connection to JupyterHub (Notebooks and Terminal)
Open the JupyterHub server login site in a new tab with [this link](https://lab.matmor.unam.mx:8443/hub/login).
Open this [Google sheet](https://docs.google.com/spreadsheets/d/1Lg633gpV8KrUqTn34PDM8V0glAkTZpHcm4CViRRz1N0/edit#gid=1473209790) in a new tab and write your name in a user.
Use this user information to log in to the JupyterHub site that you opened in the previous step.

### Open a Bash Terminal
Click on the button "New" (upper right within the "Files" section) and choose the option "Terminal" from the drop-down menu. A new tab with a terminal will open.

### Open a Jupyter Notebook with the TDA environment
Click on the button "New" (upper right within the "Files" section) and choose the option "TDA" from the drop-down menu. A new tab with a notebook will open.

## Activating Conda environments

To activate a Conda environment in the Terminal of JupyterHub you need to specify the absolute path of the environment: `conda activate /miniconda3/envs/my-environment-name`    

