# distrosetta-stone
Mapping "how do I" from distro X to Y.

# Package Queries & Management

| Task  | rpm   | dpkg |
|--- |--- |--- |
| List installed packages | `rpm -qa` | `dpkg --list` |
| List info on an installed package | `rpm -qi <packagename>` | `dpkg --status <packagename>` |
| List files in an installed package | `rpm -ql <packagename>` | `dpkg --listfiles <packagename>` |
| List installed package that owns a file | `rpm -qf <filepath>` | `dpkg -S <filepath>` |

# Repository Queries & Management



# Sources / Inspiration
For years I worked across a bunch of RISC-based Unix variants and having the Unix Rosetta Stone saved me huge amounts of time and effort.

- https://bhami.com/rosetta.html
- https://kosztkas.github.io/
- https://www.baeldung.com/linux/yum-and-apt
- https://wiki.debian.org/RPM
