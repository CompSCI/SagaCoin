# SagaCoin

SagaCoin is a PoW + PoS-based cryptocurrency.

SagaCoin uses libsecp256k1,
			  libgmp,
			  Boost1.55,
			  OR Boost1.57,  
			  Openssl1.01m,
			  Berkeley DB 4.8,
			  QT5 to compile


Block Spacing: 120 Seconds
Stake Minimum Age: 8 Hours

Port: 48544
RPC Port: 48644


BUILD LINUX (see the [Wiki](https://github.com/sagacrypto/SagaCoin/wiki/Unix-Build) for dependencies)
-----------
1) git clone https://github.com/sagacrypto/SagaCoin.git SagaCoin

2) cd SagaCoin/src

3) sudo make -f makefile.unix            # Headless SagaCoin

(optional)

4) strip SagaCoind

5) sudo cp SagaCoind /usr/local/bin




BUILD WINDOWS
-------------

1) Download Qt.zip from https://github.com/sagacrypto/SagaCoin/releases/tag/v1.0 and unpack to C:/

2) Download SagaCoin source from https://github.com/sagacrypto/SagaCoin/archive/master.zip 

2.1) Unpack to C:/SagaCoin

3) Install Perl for windows from the homepage http://www.activestate.com/activeperl/downloads

4) Download Python 2.7 https://www.python.org/downloads/windows/

4.1) While installing python make sure to add python.exe to the path.

5) Run msys.bat located in C:\MinGW49-32\msys\1.0

6) cd /C/SagaCoin/src/leveldb

7) Type "TARGET_OS=NATIVE_WINDOWS make libleveldb.a libmemenv.a" and hit enter to build leveldb

8) Exit msys shell

9) Open windows command prompt

10) cd C:/dev

11) Type "49-32-qt5.bat" and hit enter to run

12) cd ../SagaCoin

13) Type "qmake USE_UPNP=0" and hit enter to run

14) Type "mingw32-make" and hit enter to start building. When it's finished you can find your .exe in the release folder.
