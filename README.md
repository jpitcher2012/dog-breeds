# Dog Breed Catalog
This application displays a catalog of various dog breeds, categorized into the 7 AKC groups (Hound, Terrier, Working, Herding, Sporting, Non-Sporting, Toy). Users are able to log in via Google or Facebook, which then allows them to add breeds to the catalog. They are also able to edit or delete breeds that they added.

&nbsp;
## Prerequisites
- Install [Python](https://www.python.org/)
- Install [VirtualBox](https://www.virtualbox.org/)
- Install [Vagrant](https://www.vagrantup.com/)
- Install [Git](https://git-scm.com/) (optional - only needed if you want to clone the repository)

&nbsp;
## Installation
- **Option 1:** Clone GitHub repository
  - Open a terminal and navigate to where you want to install the program
  - Run the following command to clone the repository:
  
    `git clone https://github.com/jpitcher2012/dog-breeds.git`

&nbsp;
- **Option 2:** Download ZIP
  - Go to the [repository](https://github.com/jpitcher2012/dog-breeds) in GitHub
  - Click on the "Clone or download" button
  - Click "Download ZIP"
  
&nbsp;
## Program design
- This program makes use of a Linux-based virtual machine. It has a PostgreSQL database and necessary support software.
- The database includes 3 tables: 
  - The **Group** table includes information about the breed groups
  - The **Breed** table includes information about the individual breeds
  - The **User** table includes information about the application users
- There are two primary python files:
  - **models.py** has the code for the database setup
  - **views.py** has the code for running the application and handling the various endpoints
- There is helper code for adding the 7 breed groups in **add_groups.py**
 
&nbsp;
## Running the virtual machine
- Using the terminal, navigate to where you installed the code (in the **dog-breeds** directory)
- Open the **vagrant** directory
- Run the following commands to start up the virtual machine and navigate to the directory:
  - `vagrant up`
  - `vagrant ssh`
  - `cd /vagrant/catalog`
 
&nbsp;
## Starting the application
- From within the **catalog** directory, run `python views.py`. This will open the application on **localhost:5000**.

&nbsp;