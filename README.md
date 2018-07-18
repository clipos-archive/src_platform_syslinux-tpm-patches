# TPM support for Syslinux

Initiated in late 2016, the following patches serie aimed to implement a TPM
support for Syslinux 6.04.  It is based on the `syslinux-6.04-pre1` tag (commit
[bd91041](http://repo.or.cz/syslinux.git/commit/bd91041bff259cf4303fa6bbb0b6bce33fa7c1e8)).

With this patch series, Syslinux can:
* measure its modules prior to executing them;
* measure the selected kernel and the initramfs;
* measure its main configuration files.

**The current support is incomplete**, and should not be used in production as
is.  In particular, some execution path may remain uncovered where untrusted
code or text files are loaded.
