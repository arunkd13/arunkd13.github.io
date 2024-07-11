+++
title = "Passwords"
taxonomies.tags = ["tech"]
date = 2024-07-11
+++

Passwords are the simplest way for remote services to authenticate us and they
are ubiquitous. With the
number of online services we use, we try to cope by reusing passwords or making
them simple enough for us to remember. Both of these are big security risks.

To mitigate the friction of setting up passwords, many of the online services
allow to login using your Google or other major service providers. This is
technically secure, but has the risk that, if for some reason, Google determines
that you have violated their usage policy, you might end up not only [getting
locked out of your Google
services](https://www.jefftk.com/p/how-likely-is-losing-a-google-account), but
also, the entire Internet. 

Both Google Chrome and Firefox store passwords automatically in the
browser and sync them with other devices. This also would pretty secure, except
they don't provide explicit control over the files where the passwords are saved
or an explicit way to back them up.

Over the years, I have been using the [KeePassXC](https://keepassxc.org/)
software which saves account passwords and additional information in a single
encrypted file which is unlocked using a master passwords. You still need to
remember a strong master password, but remembering a few strong passwords should
not be very difficult. In fact, it is similar to reusing the same
passwords across multiple services, in terms of ease of use, but is much more
secure.

I also store this file in a [Dropbox](https://www.dropbox.com/) folder which
allows syncing with my desktop, laptop and my Android phone.

On the desktop I actually use [Secrets](https://apps.gnome.org/Secrets/), which
works with the KeePass file format and [KeePassDX](https://www.keepassdx.com/)
on Android. On iOS you can use
[Strongbox](https://apps.apple.com/us/app/strongbox-password-manager/id897283731).

Finally, to ensure that, you don't lose your passwords on any accidental
corruption, I have setup periodic backups of the password file using
[Pika](https://apps.gnome.org/PikaBackup/) on my desktop. The backups are done
to a Dropbox folder, and so, my backups reside on both my desktop and the
Dropbox cloud.

Although this setup may look more tedious than letting the browser store your
passwords and sync them, it gives me more confidence when I explcitly see where
things are stored.
