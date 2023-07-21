# Why to install npm package globally?

The main difference between local and global packages is this:

- local packages are installed in the directory where you run npm install <package-name>, and they are put in the node_modules folder under this directory
- global packages are all put in a single place in your system (exactly where depends on your setup), regardless of where you run npm install -g <package-name>

**In general, all packages should be installed locally.**

This makes sure you can have dozens of applications in your computer, all running a different version of each package if needed.

Updating a global package would make all your projects use the new release, and as you can imagine this might cause nightmares in terms of maintenance, as some packages might break compatibility with further dependencies, and so on.

All projects have their own local version of a package, even if this might appear like a waste of resources, it’s minimal compared to the possible negative consequences.

**A package should be installed globally when it provides an executable command that you run from the shell (CLI), and it’s reused across projects.**
