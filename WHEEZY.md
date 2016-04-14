DEBIAN WHEEZY recipe
====================

Python tools on wheezy are vintages.

The recipe
----------

    docker run -it --rm -v `pwd`:/simp_le -w /simp_le debian:wheezy bash

    apt-get update
    apt-get install --yes python2.7-dev python-virtualenv devscripts libjs-sphinxdoc libjs-jquery libjs-underscore
    dpkg -i dh-virtualenv_0*.deb
    mk-build-deps -ri
    dpkg-buildpackage -us -uc
    dpkg -i ../simp-le_*.deb
