LaVidaCoin integration/staging tree
================================

http://www.lavidacoin.my

* Copyright (c) 2011-2013 Litecoin Developers
* Copyright (c) 2018-2023 LaVidaCoin Developers

What is LaVidaCoin?
----------------

LaVidaCoin is a lite version of Litecoin using scrypt as a proof-of-work (PoW) algorithm.
 - 30 seconds block targets
 - subsidy halves in 5 million blocks (~4 years)
 - ~766 million total coins
 - 76.6 coins per block
 - 10 minutes blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the LaVidaCoin client sofware, see http://www.lavidacoin.my.

License
-------

LaVidaCoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the LaVidaCoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of LaVidaCoin.

Find LaVidaCoin
---------------
* Website: http://www.lavidacoin.my
* Wallet: https://wallet.lavidacoin.my
* Pool : http://pool.lavidacoin.my
* Pool 2 : http://lavidapool.sytes.net:5000
* Explorer: http://explorer.lavidacoin.my

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

    qmake BITCOIN_QT_TEST=1 -o Makefile.test lavidacoin-qt.pro
    make -f Makefile.test
    ./lavidacoin-qt_test

