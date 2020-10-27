|[Introduction to Linux](Linux_1.md)  | [Operating Systems](Linux_2.md) |

# Day 4
# Operating Systems
Modern operating systems don’t just manage hardware and software resources, they schedule programs to run in a multi-tasking manner (sharing the processor so that multiple tasks can occur apparently simultaneously), provide standard services that allow users and programs to request something happen (for example a print job) from the operating system, and provided it’s properly requested, the operating system will accept the request and perform the function needed.
![image](https://ndg-content-dev.s3.amazonaws.com/media/images/linux-essentials-v2/LEv2_2_1.png)
## Computer users today have a choice mainly between three major operating systems: 
- Microsoft Windows -- underlying code.
- Apple macOS -- a fully-qualified UNIX distribution based on BSD Unix.
- and Linux --  can be any one of hundreds of distribution packages designed or optimized for whatever task is required.
##  Decision Points
# Day 6
1. *Role*
- Will you be sitting at the console running productivity applications or web browsing? If so, a familiar desktop is best.
- Will the machine be accessed remotely by many users or provide services to remote users? Then it’s a server.
Servers generally run as a CLI, which frees up resources for the real purpose of the computer: serving information to clients.
2. *Function*
Is there specific software it needs to run, or specific functions it needs to perform? Will there be hundreds, even thousands, of these machines running at the same time? What is the skill-set of the team managing the computer and software?
3. *Life Cycle*
Operating systems and software upgrades come on a periodic basis, called a release cycle.
Vendors only support older versions of software for a certain period of time before not offering any updates; this is called a maintenance cycle or life cycle.
4. ‌⁠​​⁠​*Stability*
Individual software releases can be characterized as beta ( When a software release has many new features that haven’t been tested, it’s typically referred to as beta.) or stable depending on where they are in the release cycle. 
5. *Compatibility*
Another loosely-related concept is backward compatibility which refers to the ability of later operating systems to be compatible with software made for earlier versions. 
 The common practice of maintaining and versioning libraries of functions helps this greatly.
6. *Cost*
7. *Interface*
The first electronic computer systems were controlled by means of switches and plugboards similar to those used by telephone operators at the time. Then came punch cards and finally a text-based terminal system similar to the Linux command line interface (CLI) in use today. The graphical user interface (GUI), with a mouse and buttons to click, was pioneered at Xerox PARC (Palo Alto Research Center) in the early 1970s and popularized by Apple Computer in the 1980s.
##  Linux
Linux users typically obtain an operating system by downloading a distribution. A Linux distribution is a bundle of software, typically comprised of the Linux kernel, utilities, management tools, and even some application software in a package which also includes the means to update core software and install additional applications.
### Life Cycle
Most distributions have both major and minor update cycles to introduce new features and fix existing bugs. Additionally, there are development packages where users can contribute code and submit patches for possible inclusion into new releases.

Linux distributions can be broadly classed in two main categories: enthusiast and enterprise. An enthusiast distribution such as openSUSE’s Tumbleweed has a fast update cycle, is not supported for enterprise and may not contain (or drop) features or software in the next version that are in the current one. Red Hat’s Fedora project uses a similar method of development and release cycle, as does Ubuntu Desktop.

Enterprise distributions are almost the exact opposite, in that they take care to be stable and consistent, and offer enterprise-grade support for extended periods, anywhere from 5-13 years in the case of SUSE. Enterprise distributions are fewer by far, being offered mainly by Red Hat, Canonical and SUSE.
### Cost
Your chosen Linux distribution itself might be zero cost, but paying for support may be worthwhile depending on organizational needs and capabilities.
### Interface
- Like most operating systems, Linux can be used in one of two ways: graphical (GUI) and non-graphical (CLI). Below is an example of a graphical desktop, with a menu bar of popular applications to the left, a LibreOffice document being edited in the foreground, and a web browser in the background.
![image](https://ndg-content-dev.s3.amazonaws.com/media/images/linux-essentials-v2/LEv2_2_2.png)

- The second type of interface, the CLI, is a text-based interface to the computer, where the user types in a command and the computer then executes it. The CLI environment is provided by an application on the computer known as a terminal. ‌⁠​⁠​The terminal accepts what the user types and passes to a shell. The shell interprets what the user has typed into instructions that can be executed by the operating system. If output is produced by the command, then this text is displayed in the terminal. If problems with the command are encountered, then an error message is displayed.

