|[Introduction to Linux](Linux_1.md)  | [Operating Systems](Linux_2.md) |
[navigatingTheLinuxDesctop](Linux_3.md) 
# Day 8
# Navigating the Linux Desktop
Each Linux desktop distribution is slightly different, but the application terminal or x-term will open a terminal window from the GUI.
The **kernel** of the operating system is like an air traffic controller at an airport, and the applications are the airplanes under its control. The kernel decides which program gets which blocks of memory, it starts and kills applications, and it handles displaying text or graphics on a monitor.
The kernel also abstracts some complicated details away from the application. For example, the application doesn’t know if a block of disk storage is on a solid-state drive, a spinning metal hard disk, or even a network file share. Applications need only follow the kernel’s Application Programming Interface (API) and therefore don’t have to worry about the implementation details. Each application behaves as if it has a large block of memory on the system; the kernel maintains this illusion by remapping smaller blocks of memory, sharing blocks of memory with other applications, or even swapping out untouched blocks to disk.**يا كرنل يا ختير**
The kernel also handles the switching of applications, a process known as multitasking.
A process is just one task that is loaded and tracked by the kernel. An application may even need multiple processes to function, so the kernel takes care of running the processes, starting and stopping them as requested, and handing out system resources.

*Linux software generally falls into one of three categories:*
- Server Applications:
Software that has no direct interaction with the monitor and keyboard of the machine it runs on. Its purpose is to serve information to other computers, called clients.Linux excels at running server applications because of its reliability and efficiency. 
- Desktop Applications:
Web browsers, text editors, music players, or other applications with which users interact directly. 
- Tools
A loose category of software that exists to make it easier to manage computer systems. Tools can help configure displays, provide a Linux shell that users type commands into, or even more sophisticated tools, called compilers, that convert source code to application programs that the computer can execute.

## Web servers
WordPress,Apache and NGINX..
Over 65% of websites are powered by either NGINX or Apache.

## Private Cloud Servers
As individuals, organizations, and companies start to move their data to the cloud, there is a growing demand for private cloud server software that can be deployed and administered internally.
nextcloud,owncloud.

## Database Servers
A database stores information and also allows for easy retrieval and querying. Some other popular databases are Firebird and PostgreSQL. You might enter raw sales figures into the database and then use a language called Structured Query Language (SQL) to aggregate sales by product and date to produce a report.

## File Sharing
For Windows-centric file sharing, Samba is the clear winner. Samba allows a Linux machine to look and behave like a Windows machine so that it can share files and participate in a Windows domain. 

## *Desktop Applications*
The Linux ecosystem has a wide variety of desktop applications. There are games, productivity applications, creative tools, web browsers and more.

## Web Browsers
Linux is a first class citizen for the Mozilla Firefox and Google Chrome browsers. Both are open source web browsers that are fast, feature-rich, and have excellent support for web developers.
the Internet has two excellent browsers that push the limits of what can be done on the web, and work across a variety of platforms. Using a browser, while second nature for many, can lead to privacy concerns. By understanding and modifying the configuration options, one can limit the amount of information they share while searching the web and saving content.
## shells
At the basic level, users interact with a Linux system through a shell whether connecting to the system remotely or from an attached keyboard.
Linux offers a variety of shells to choose from, mostly differing in how and what can be customized, and the syntax of the built-in scripting language. The two main families are the *Bourne shell* and the *C shell*.
## Text Editors
commonly used at the console to edit configuration files. The two main applications are *Vi* (or the more modern Vim) and *Emacs*. Both are remarkably powerful tools to edit text files; not helpful for simple editing of a small text file. *Pico and Nano* are available on most systems and provide very basic text editing.
## Package Management
**packages**, which are compressed files that bundle up an application and its dependencies (or required files), greatly simplifying the installation by making the right directories, copying the proper files into them, and creating such needed items as symbolic links.
**A package manager** takes care of keeping track of which files belong to which package and even downloading updates from repositories,the two most popular are those from Debian and Red Hat.
- Debain
 files ending in the .deb extension. Ubuntu and Mint.
 The lowest-level tool for managing these files is the `dpkg` command. This command can be tricky for novice Linux users, so the Advanced Package Tool, `apt-get` (a front-end program to the dpkg tool), makes management of packages easier. Additional command line tools which serve as front-ends to `dpkg` include `aptitude` and GUI front-ends like Synaptic and Software Center.
- RPM Package Management
 RPM makes use of an .rpm file for each software package.
 The back-end tool most commonly used for RPM Package Management is the `rpm` command. While the `rpm` command can install, update, query and remove packages, the command line front-end tools such as `yum` and `up2date` automate the process of resolving dependency issues.
 Some RPM-based distributions have implemented the ZYpp (or libzypp) package management style, mostly openSUSE and SUSE Linux Enterprise, but mobile distributions MeeGo, Tizen and Sailfish as well.

 The `zypper` command is the basis of the ZYpp method, and it features short and long English commands to perform functions, such as `zypper` in `packagename` which installs a package including any needed dependencies.

 Most of the commands associated with package management require root privileges. The rule of thumb is that if a command affects the state of a package, administrative access is required. In other words, a regular user can perform a query or a search, but to add, update or remove a package requires the command to be executed as the root user.
## language
Linux itself was written in a compiled language called C.
**JavaScript** is a high-level interpreted programming language that is one of the core technologies on the world wide web. It is similar to but fundamentally different from Java, which is a completely object-oriented programming language owned by Oracle. JavaScript is a cross-platform scripting language for adding interactive elements to web pages, that is in wide use across the internet. By using JavaScript libraries, web programmers can add everything from simple animations to complex server-side applications for internet users. JavaScript is continuously evolving to meet the functionality and security needs of internet users and is capable of being released under a GNU GPL License.
Perl is an interpreted language. Perl was originally developed to perform text manipulation. Over the years, it gained favor with systems administrators and continues to be improved and used in everything from automation to building web applications.

**PHP** is a language that was initially built to create dynamic web pages. A PHP file is read by a web server such as Apache. Special tags in the file indicate that parts of the code should be interpreted as instructions. The web server pulls all the different parts of the file together and sends it to the web browser. PHP’s main advantages are that it is easy to learn and available on almost any system. Because of this, many popular projects are built on PHP. Notable examples include WordPress (for blogging), cacti (for monitoring), and even parts of Facebook.

**Ruby** is another language that was influenced by Perl and Shell, along with many other languages. It makes complex programming tasks relatively easy, and with the inclusion of the Ruby on Rails framework, is a popular choice for building complex web applications. Ruby is also the language that powers many of the leading automation tools like Chef and Puppet, which make managing a large number of Linux systems much simpler.

**Python** is another scripting language that is in general use. Much like Ruby it makes complex tasks easier and has a framework called Django that makes building web applications very easy. Python has excellent statistical processing abilities and is a favorite in academia.

A computer programming language is just a tool that makes it easier to tell the computer what you want it to do. A library bundles common tasks into a distinct package that can be used by the developer. **ImageMagick** is one such library that lets programmers manipulate images in code. ImageMagick also ships with some command line tools that enable programmers to process images from a shell and take advantage of the scripting capabilities there.

**OpenSSL** is a cryptographic library that is used in everything from web servers to the command line. It provides a standard interface for adding cryptography into a Perl script, for example.
## Password Issues
There are many levels of access and various means of password management on a Linux system. When users are created, they are given different login permissions depending on what groups they are assigned to. For example, administrators can create and manage users while regular users cannot. Services that run on systems such as databases can also have login permissions with their own passwords and privileges. Additionally, there are specific passwords for accessing systems remotely through SSH, FTP, or other management programs.
 Passwords need to be complex enough not to be easily guessed by hackers, yet easy to remember for users.
  Use a password manager like KeePassX to generate passwords, and then you only need to have a login password to your machine and a password to open up your KeePassX file.

## The Cloud
A cloud deployment model provides a basis for how cloud infrastructure is built, managed, and accessed. There are four primary cloud deployment models:
- Public Cloud: A public cloud is a cloud infrastructure deployed by a provider to offer cloud services to the general public and organizations over the Internet.
- Private Cloud: A private cloud is a cloud infrastructure that is set up for the sole use of a particular organization.
- Community Cloud: A community cloud is a cloud infrastructure that is set up for the sole use by a group of organizations with common goals or requirements.
- Hybrid Cloud: A hybrid cloud is composed of two or more individual clouds, each of which can be a private, community, or public cloud. A hybrid cloud may change over time as component clouds join and leave.
##  Linux in the Cloud
Linux plays a pivotal role in cloud computing. It powers 90% of the public cloud workload, most virtual servers are based on some version of the Linux kernel, and Linux is often used to host the applications behind cloud computing services. offers:
- Flexibility :Cloud computing provides the capability to provision IT resources quickly and at any time.Linux stands out here because it is highly adaptable.
- Accessibility
- Cost-Effective
- Manageability
- Security
- Virtualization :Virtualization is one of the most significant advancements that has contributed to the enablement cloud of computing.Linux is a multi-user operating system, which means that many different users can work on the same system simultaneously.
- 

