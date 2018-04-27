Opioid integration/staging tree
================================

https://oid.life

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2018 Opioid Developers

What is Opioid?
----------------

Opioid is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 2 minute block targets
 - subsidy halves in 210k blocks (~3 years)
 - ~214,285,714 million total coins

The rest is the same as Bitcoin; however with updated stadards.
 - 500 coins per block. 
 - 50 coins towards dev fees (from pools). 
 (Please see code of conduct -> https://github.com/OidLife/Conduct)
 - 2016 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Opioid client sofware, see https://github.com/OidLife/opioid-oid-project . 

License
-------

Opioid is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Opioid
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/OidLife/opioid-oid-project) are created
regularly to indicate new official, stable release versions of Opioid.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake OPIOID_QT_TEST=1 -o Makefile.test Opioid-qt.pro
    make -f Makefile.test
    ./opioid-qt_test

### If you plan on compiling from source, please make sure the seed nodes are pointed to:
1) `oidseednode1.net`
2) `oidseednode2.net`

Refer to /src/ -> net.cpp beginning @ line 1178

``static const char *strMainNetDNSSeed[][2] = {  
    {"oidseednode1.net", "oidseednode1.net"},  
    {"oidseednode2.net", "oidseednode2.net"},  
    {NULL, NULL}  
};``

Thank you,

OID Team
