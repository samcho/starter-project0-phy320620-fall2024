# Project 0: Becoming Familiar with the Ubuntu Linux Environment

Note: You are strongly encouraged to work together.  However, each person is responsible for producing and submitting their own work.

The DEAC High Performance Computing (HPC) Cluster consists of about 100 nodes, 4,000 CPU cores, 70,000 GPU cores, 20 TB of memory, and 300 TB of disk space. It is a powerful shared resource among Wake Forest University professors, research scientists, students, and collaborators, and we will use it to perform MD simulations in our class. 

If a DEAC HPC Cluster account does not already exist due to your ongoing research project, a new account was created for you.

## Part 1 Log into the DEAC HPC Cluster

When you log into the DEAC HPC Cluster, are you actually logging into a _head node_ that acts as a gateway to other resources. A head node is configured to submit jobs to the _scheduler_ that looks for an available _node_ and runs your work without interferring with the work of others.

![image](https://github.com/user-attachments/assets/de24cecb-3bb7-4650-981e-ae3c9fc368e5)

The DEAC HPC Cluster nodes are __gemini.deac.wfu.edu__ and __pegasus.deac.wfu.edu__, which should be the same (Dr. Cho uses "gemini" mostly because he sometimes misspells "pegasus").

The DEAC HPC Cluster head nodes are restricted to Wake Forest University Networks for security reasons. If you are off campus, you must have an [established VPN connection](https://is.wfu.edu/vpn/) to vpn.wfu.edu.

To login to the DEAC HPC Cluster, you need to use a client (i.e., program) that supports Secure SHell (SSH) to set up an encrypted terminal session to a head node.

### For Windows Users
PowerShell is a terminal program that comes bundled with every supported version of Windows. To start it, open the __Start__ menu, type __Windows PowerShell___, then select __Open__.

## For Mac OS X Users
Terminal is a terminal program that comes bundled with every supported version of Mac OS X. To start it, select the magnifying glass icon at the top right, type __Terminal__, then press the __return__ button.

In either PowerShell or Terminal, type the following command (replacing "username" with your username):

```
ssh -Y username@gemini.deac.wfu.edu
```

You will be prompted to enter your password, which you need to enter (Note: The cursor will not move when you enter the password.). 

Upon successful login, you will see the following banner:

```

******************************************************************************
*  Unauthorized use is STRICTLY PROHIBITED and WFU maintains all rights to   *
*  University related or legal actions associated with such access. Refer    *
*  to https://go.wfu.edu/deac-sla for detailed documentation and policies.   *
******************************************************************************

******************************************************************************
*  Wake Forest University -- Distributed Environment for Academic Computing  *
*                                                                            *
* __/\\\\\\\\\\\_____/\\\\\\\\\\\\\____/\\\\\\\\___________/\\\\\\\_________ *
* __\/\\\///////\\\__\/\\\/////////___/\\\\\\\\\\\\______/\\\//////_________ *
* ___\/\\\_____\//\\\_\/\\\___________/\\\////////\\\___/\\\/_______________ *
* ____\/\\\______\/\\\_\/\\\\\\\\\____\/\\\______\/\\\__/\\\________________ *
* _____\/\\\______\/\\\_\/\\\/////_____\/\\\\\\\\\\\\\\_\/\\\_______________ *
* ______\/\\\______\/\\\_\/\\\__________\/\\\////////\\\_\//\\\_____________ *
* _______\/\\\______/\\\__\/\\\__________\/\\\______\/\\\__\///\\\__________ *
* ________\/\\\\\\\\\\\/___\/\\\\\\\\\\\\\\/\\\______\/\\\____\////\\\\\\\__ *
* _________\///////////_____\/////////////_\///_______\///________\///////__ *
*                                                                            *
*  For questions and support, email deac-help@wfu.edu. You must acknowledge  *
*  the WFU HPC Facility in publications: https://go.wfu.edu/deac-doi         *
*                                                                            *
******************************************************************************
```

## Part 2 Log into the DEAC HPC Cluster
The Linux operating system is world's most widely used operating system, and it is installed on mobile devices, televisions, applicances, automobiles, and spacecraft. In addition, it is the world's most popular operating system on high performance computing facilities, including the DEAC HPC Cluster. The Linux environment is very rich with lots of different functionality. Our goal is not to learn all of Linux (no one can!), but to learn just enough for us to perform MD simulaions.

The following is a very small list of commands that you might find useful for getting started. Use it as a reference.

### Basic Commands
| Command | What it does|
| --- | --- |
| ls	| displays a list of files in the current directory |
| ls -l	| displays a detailed list of files in the current directory |
| cd __directory__	| changes the current directory to a new directory |
| cp __source__ __destination__	| copies a file from the source location to a new destination |
| rm __file__	| deletes a file |
| mkdir __directory__	| creates a new directory |
| rmdir __directory__	| removes an existing empty directory; error message if not empty |
| pwd	| displays the current directory |
| exit	| log out of the session |
| ssh -Y __host__	| remote log into a host |

### Learning Linux by Example
The quickest way to learn to do a lot of things very quickly is to just go ahead and jump in. Repeat the commands in the screenshot replacing "choss" with your username.

![image](https://github.com/user-attachments/assets/ad1e89de-99af-49af-8732-19d3f390d509)

## Part 3 Transferring Files Between Your Compter and the DEAC HPC Cluster

Since the DEAC HPC Cluster is a remote site where supercomputing is done you will need to transfer the results back to your computer (or send it back). One way to do this is to user a file transfer client like [Filezilla](https://filezilla-project.org/). It is a drag and drop environment and fairly straightforward to use.

## Part 4 Git

Git is a powerful program to keep track of different versions of a program. It has many different functionality. Our goal is not to learn all of Git, but just enough to make copies of repositories that hold MD simulation setup information and data that Dr. Cho has placed into Github repositories like this one.

Log back into the DEAC HPC Cluster (See Part 2).

Go to your directory.

Clone this repository using the following command (replacing "<repository url>" with the web URL of this repository):

```
git clone <repository url>
```

You should see in your directory an exact copy of this __README.md__ file.

For this portion, I want you to make a modification to this file, commmit the modification, and push the change to the repository. If you need help doing this portion, not to worry, we will go over it in class, and I am also happy to help during office hours.
