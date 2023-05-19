# distrosetta-stone
Mapping "how do I" from distro X to Y.

This won't be hugely comprehensive (unless it becomes so over time), but I'm jumping from Red Hat-based distros where I don't have to think about "how to X" to Debian-based distros, where I do.  There's loads of great resources out there on the differences / translation but I wanted something *condensed*.

# Package Queries &  Management

| Task  | rpm | dpkg |
|--- |--- |--- |
| List all installed packages | `rpm -qa` | `dpkg --list` |
| List info on an installed package | `rpm -qi <packagename>` | `dpkg --status <packagename>` |
| List all files in an installed package | `rpm -ql <packagename>` | `dpkg --listfiles <packagename>` |
| List key config files in an installed package | `rpm -qc <packagename>` | `cat /var/lib/dpkg/info<packagename>.conffiles`  |
| List key documentation files in an installed package | `rpm -qd <packagename>` |  |
| List installed package that owns the file | `rpm -qf <filepath>` | `dpkg -S <filepath>` |
| List info on a package file | `rpm -qpi <packagename.rpm>` | `dpkg --info <packagename.deb>` |
| List all files in a package file | `rpm -qpl <packagename.rpm>` | `dpkg --contents <packagename.deb>` |
| List key config files in a package file | `rpm -qpc <packagename>` |  |
| List key documentation files in a package file | `rpm -qpd <packagename>` |  |

# Repository Queries &  Management

| Task  | yum | apt |
|--- |--- |--- |
| List all installed packages | `yum list installed` | `apt list --installed` |
| List all available packages | `yum list available` | `` |
| List all installed and available packages | `yum list all` | `apt list` |
| List all installed and available packages for a package | `yum list <packagename>` | `apt list \| grep -v installed` |


# Sources / Inspiration
For years I worked across a bunch of RISC-based Unix variants and having the Unix Rosetta Stone saved me huge amounts of time and effort.

- https://bhami.com/rosetta.html
- https://kosztkas.github.io/
- https://www.baeldung.com/linux/yum-and-apt
- https://wiki.debian.org/RPM
