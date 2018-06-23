![ALMA](images/beautiful.jpg)
[Image source](http://alma.asiaa.sinica.edu.tw/_img/site_multimedia/2013AOS/IMG_4017.jpg)

## Weekly report 2018/06/18~2018/06/24
#### 1. Trace carta
* [protobuf tester](https://github.com/CARTAvis/carta/pull/258)
#### 2. read issues/pull requests
#### 3. license study

## [TODO]Weekly report 2018/06/25~2018/07/01

## Weekly report 2018/06/11~2018/06/17

#### 1. micro web socket study
* [uWebSockets](https://github.com/uNetworking/uWebSockets)
* WebSocket implementation for c++, javascript(Node.js)
* 目前号称最高性能的websocket c++库
* [Comparison of WebSocket implementations](https://en.wikipedia.org/wiki/Comparison_of_WebSocket_implementations)
* [TODO][github repo of my practice:]
* possible entry in CARTA? 

#### 2. build carta viewer again on CentOS
* [CARTA viewer](https://github.com/CARTAvis/carta)
* $ sudo ./CARTAvis/carta/scripts/buildcasa.sh
``` 
CMake Error at install/config.cmake:836 (message):
  WCSLIB could not be found.  Please check!
Call Stack (most recent call first):
  CMakeLists.txt:961 (casa_find)
  
  
-- Configuring incomplete, errors occurred!
See also "/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/casa/trunk/code/build/CMakeFiles/CMakeOutput.log".
See also "/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/casa/trunk/code/build/CMakeFiles/CMakeError.log".
make: *** No targets specified and no makefile found.  Stop.
```
* still errors in make -j2, need to check it out
```
make[3]: Entering directory `/home/duidae/projects/CARTA/CARTAvis/build/cpp/plugins/RegionCASA'
cp -f /home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/RegionCASA/plugin.json plugin.json
g++ -c -pipe -DCARTA_RUNTIME_CHECKS=1 -O2 -fopenmp -Wall -W -std=c++0x -D_REENTRANT -fPIC -DUseCasacoreNamespace=1 -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I/opt/Qt/5.3/gcc_64/mkspecs/linux-g++ -I/home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/RegionCASA -I/home/duidae/projects/CARTA/CARTAvis/carta/cpp -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/casa/trunk/linux/include -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/casa/trunk/linux/include/casacore -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/wcslib/include -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/cfitsio/include -I/home/duidae/projects/CARTA/CARTAvis/ThirdParty/imageanalysis/include -I/opt/Qt/5.3/gcc_64/include -I/opt/Qt/5.3/gcc_64/include/QtGui -I/opt/Qt/5.3/gcc_64/include/QtCore -I. -I. -o RegionCASA.o /home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/RegionCASA/RegionCASA.cpp
In file included from /home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/RegionCASA/RegionCASA.cpp:1:0:
/home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/RegionCASA/RegionCASA.h:9:54: 嚴重錯誤：imageanalysis/Annotations/AnnotationBase.h：沒有此一檔案或目錄
 #include "imageanalysis/Annotations/AnnotationBase.h"
                                                      ^
編譯插斷。
make[3]: *** [RegionCASA.o] Error 1
make[3]: Leaving directory `/home/duidae/projects/CARTA/CARTAvis/build/cpp/plugins/RegionCASA'
make[2]: *** [sub-RegionCASA-make_first] Error 2
make[2]: *** Waiting for unfinished jobs....
g++ -c -pipe -DCARTA_RUNTIME_CHECKS=1 -O2 -fopenmp -Wall -W -std=c++0x -D_REENTRANT -fPIC -DUseCasacoreNamespace=1 -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I/opt/Qt/5.3/gcc_64/mkspecs/linux-g++ -I/home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/ImageStatistics -I/home/duidae/projects/CARTA/CARTAvis/carta/cpp -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/casa/trunk/linux/include -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/casa/trunk/linux/include/casacore -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/wcslib/include -I/home/duidae/projects/CARTA/CARTAvis-externals/ThirdParty/cfitsio/include -I/home/duidae/projects/CARTA/CARTAvis/ThirdParty/imageanalysis/include -I/opt/Qt/5.3/gcc_64/include -I/opt/Qt/5.3/gcc_64/include/QtGui -I/opt/Qt/5.3/gcc_64/include/QtCore -I. -I. -o StatisticsCASARegion.o /home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/ImageStatistics/StatisticsCASARegion.cpp
/home/duidae/projects/CARTA/CARTAvis/carta/cpp/plugins/ImageStatistics/StatisticsCASARegion.cpp:4:62: 嚴重錯誤：imageanalysis/ImageAnalysis/ImageStatsCalculator.h：沒有此一檔案或目錄
 #include "imageanalysis/ImageAnalysis/ImageStatsCalculator.h"
                                                              ^
編譯插斷。
make[3]: *** [StatisticsCASARegion.o] Error 1
make[3]: *** Waiting for unfinished jobs....
make[3]: Leaving directory `/home/duidae/projects/CARTA/CARTAvis/build/cpp/plugins/ImageStatistics'
make[2]: *** [sub-ImageStatistics-make_first] Error 2
make[2]: Leaving directory `/home/duidae/projects/CARTA/CARTAvis/build/cpp/plugins'
make[1]: *** [sub-plugins-make_first] Error 2
make[1]: Leaving directory `/home/duidae/projects/CARTA/CARTAvis/build/cpp'
make: *** [sub-cpp-make_first] Error 2
```

#### 3. computer change to MacbookPro
* ok

#### 4. study CASA
* [CASA](https://casa.nrao.edu/)
* running on Redhat 6/7 & Mac OS X
* difference between Redhat/CentOS: CentOS is a community-developed and supported alternative to RHEL(Red Hat Enterprise Linux). It is similar to Red Hat Enterprise Linux but lacks the enterprise-level support. CentOS is more or less a free replacement for RHEL with few minor configuration differences.
* [TODO] build on RHEL

#### 5. install CentOS, RHEL for practice
* ok
* RHEL needs $$, ALMA Taiwan ARC uses CentOS 7.2(ALMA T1~T7)
![centos](images/centos+RHEL.png)

## Weekly report 2018/06/04~2018/06/10

#### 0. webpage for working progress
* ok
* [webpage](https://duidae.github.io/Asiaa-work/)

#### 1. Google protocol buffers study
* smaller, faster, binary message structure like json
* protocol buffers: [https://developers.google.com/protocol-buffers/](https://developers.google.com/protocol-buffers/)
* [Overview](https://developers.google.com/protocol-buffers/docs/overview), [Tutorials](https://developers.google.com/protocol-buffers/docs/tutorials), [Github](https://github.com/google/protobuf/releases)
* .proto defines message strucuture, compiler generates corresponding .h .cc file
* github repo of my practice: [cpp only(modified makefile)](https://github.com/duidae/Asiaa-work/tree/master/protobuf-example)
* possible entry in CARTA? our protobuf message structure?
* good solution for large size json needed encryption

#### 2. qt creator installation 
* ok
![qt creator](images/2018-06-09%2019-03-55%20qtcreator.png)

#### 3. preparation for report on 7/2
* computer discuss with Mark, spec ok
* necessary materials for Vicky in advance, ok

#### 4. docker study
* docker cookbook, O'reilly
![qt creator](images/docker.jpg)

#### 5. DevOps
* really helpful article...[github, CircleCI, docker](http://blog.amowu.com/2015/04/devops-continuous-integration-delivery-docker-circleci-aws-beanstalk.html)
![devop sequence diagram](images/sequence-diagram.png)

#### 5. how to do open source development/run open source project
* Innovation Happens Elsewhere (Version 1.0) [Nice ebook](https://www.dreamsongs.com/IHE/)

## Pull request
* [Fix] typo/delete/modify in /home/duidae/projects/CARTA/CARTAvis/carta/scripts/buildcasa.sh // 整理buildcasa.sh
    * typo: 3 ## TODO: remove installinging
    * delete: 77     #### install Qt 4.8.5
    * delete: 78     # sudo yum -y install qt-devel.x86_64
    * delete: 79     # alias qmake='qmake-qt4'
    * remove commented code
    * comment註明路徑(casa, casacore)
    * 282 cd ../../code  //是否改成cd $casawork/trunk/code 較易讀
* [Fix] carta/readme.txt -> carta/readme.md // change readme.txt to markdown 

## Reference
* [ALMA](http://www.almaobservatory.org/en/home/)
* [ALMA @ Asiaa](http://alma.asiaa.sinica.edu.tw/index.php)
  * [Fix]deadlink http://almat3.asiaa.sinica.edu.tw/ganglia/
  * Interesting & beautiful, rock band?!! http://alma.asiaa.sinica.edu.tw/intro_multimedia.php
  * AcidMan: ALMA https://www.youtube.com/watch?v=ylEDfirYJaY
* [ALMA kids](http://kids.alma.cl/?lang=zh)
* [ALMA sounds(art)](http://www.almasounds.org/)
* 譬喻：從墾丁看到台北101頂端的一隻金龜子
* [CASA](https://casa.nrao.edu/)
* [Code NASA](https://code.nasa.gov/)
* [Data NASA](https://data.nasa.gov/)
* markdown syntax: [mastering markdown](https://guides.github.com/features/mastering-markdown/), [chinese](https://github.com/othree/markdown-syntax-zhtw)

## C++
* lambda expression(anonymous function)
  * [https://en.wikipedia.org/wiki/Anonymous_function#C++_(since_C++11)](https://en.wikipedia.org/wiki/Anonymous_function#C++_(since_C++11))
  * [http://en.cppreference.com/w/cpp/language/lambda](http://en.cppreference.com/w/cpp/language/lambda)
  * [https://msdn.microsoft.com/zh-tw/library/dd293608.aspx](https://msdn.microsoft.com/zh-tw/library/dd293608.aspx)
  * [https://kheresy.wordpress.com/2010/05/27/c0x%EF%BC%9Alambda-expression/](https://kheresy.wordpress.com/2010/05/27/c0x%EF%BC%9Alambda-expression/)
* STL documentation:
  * [http://www.cplusplus.com/reference/stl/](http://www.cplusplus.com/reference/stl/)

## Questions
* why not open source CASA directly?
* do we use Slack?
