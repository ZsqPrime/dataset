dbslayer patched
================

Please take note of the AUTHORS and LICENSE for this repo.
Only the authors can offer you specific license terms.
This repo is licensed per the LICENSE file

once you have replicated this repo
you'll need the following pacakges installed before you can compile

use apt-get to install these packages

mysql-client-core-5.5 libapr1-dev libaprutil1-dev apache2-utils autoconf

e.g.

```bash
sudo apt-get install mysql-client-core-5.5 libapr1-dev libaprutil1-dev apache2-utils autoconf
```

then do a

```bash
./configure
make
sudo make install
```

Other instructions can be found in the INSTALL file
