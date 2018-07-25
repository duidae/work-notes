![ALMA](images/beautiful.jpg)
[Image source](http://alma.asiaa.sinica.edu.tw/_img/site_multimedia/2013AOS/IMG_4017.jpg)
## CARTA team
* [Slack](https://cartaviewer.slack.com/messages/C2S1R8V9P/)
* [Trello](https://trello.com/b/fViU1U7v/carta-working-group)

## Weekly progress 2018/07/23~2018/07/29
#### 1. Trace frontend
* normal structure of Typescript+React:
  * myapp/
    * node_modules/
    * public/: public	 包含了静态资源如HTML页面或图片。除了 	index.html	 文件外,其它的文件都可以删除。
    * src/: 包含了TypeScript和CSS源码。 	index.tsx是强制使用的入口文件。
    * package.json: 包含了依赖,还有一些命令的快捷方式
    * tsconfig.json: TypeScript特定的选项
    * tslint.json: 代码检查器的设置
* Frameworks/tools
  * Typescript - 語言
  * React - JS UI library
  * Typescript + React
    * https://github.com/Microsoft/TypeScript-React-Starter
  * MobX - State management
    * https://mobx.js.org/getting-started.html
  * GoldenLayout - UI layout
    * http://golden-layout.com/tutorials/getting-started-react.html
  * Blueprint - UI component
    * http://blueprintjs.com/docs/
    * core - UI元件
    * icon - 圖
    * 看document用比較快
  * 從這些東西的Getting Started去了解最快
* Trace CARTA-frontend (Angus's code)
  * Angus應該是用[MS TypeScript React Starter](https://github.com/Microsoft/TypeScript-React-Starter)建構frontend structure, 檔案結構一樣
  ![Typescript+React](images/file-structure.png)
  * src/
    * [X] index.tsx
      * index.tsx是强制使用的入口文件。
    * [ ] App.tsx
    * [X] registerServiceWorker.ts
      * Create-React-App產生
      * service worker是在后台运行的一个线程，可以用来处理离线缓存、消息推送、后台自动更新等任务。registerServiceWorker就是为react项目注册了一个service worker，用来做资源的缓存，这样你下次访问时，就可以更快的获取资源。而且因为资源被缓存，所以即使在离线的情况下也可以访问应用（此时使用的资源是之前缓存的资源）。注意，registerServiceWorker注册的service worker 只在生产环境中生效（process.env.NODE_ENV === 'production'）
    * [ ] components/
      * Colormap
      * Dialogs
      * ImageView
      * Log: 左下角的Log
      * Menu: 最上面的menu - File, View, Layout, Help
      * Placeholder
      * SpatialProfiler
    * [X] models/
      * MVC的M
      * Point2D, CursorInfo
    * [ ] services/
      * BackendService
      * DecompressionService
    * [ ] stores/
      * SSOT(Single Source of Truth)：資料統一存放於 Store，View 要資料都需跟 Store 拿。

#### 2. Related techs
* Facebook
  * React
  * create-react-app
    * https://github.com/facebook/create-react-app
  * Jest
    * https://jestjs.io/
    * https://github.com/facebook/jest
* Microsoft
  * Typescript
  * Typescript + React starter
    * https://github.com/Microsoft/TypeScript-React-Starter
* Mobx
  * https://cn.mobx.js.org/
* Redux
  * Redux is an open-source JavaScript library for managing application state. It is most commonly used with libraries such as React or Angular for building user interfaces.
* RxJS
  * https://blog.techbridge.cc/2017/12/08/rxjs/
* Javascript @ W3C school
  * https://www.w3schools.com/js
    
#### 3. Typescript
* 什麼是 Duck Typing 與 Strong Typing ?
  * Duck typing
    * Duck Typing: 當看到一隻鳥走起來像鴨子、游泳起來像鴨子、叫起來也像鴨子，那麼這隻鳥就可以被稱為鴨子。
    * 白話 : 物件只要有該型別相同的 property 與 method，就算是該 class 型別。
    * JavaScript 採用的是 duck typing
  * Strong typing
    * 由母鴨生產的鴨子，才算是鴨子。
    * 白話 : 物件必須透過 class 的 new 建立，物件才算是該 class 型別。
* TypeScript 因為要相容 JavaScript，且最後也是編譯成 JavaScript，所以 TypeScript 本質是 duck typing，卻在編譯階段檢查型別是否正確，算是融合 strong typing 與 duck typing。
* .ts vs .tsx
  * .tsx 有用 JSX https://blog.techbridge.cc/2016/04/21/react-jsx-introduction/
  * https://eyesofkids.gitbooks.io/react-basic-zh-tw/content/day15_jsx/
```
<h1>{this.props.text}</h1>
```
  * 那麼這一段是什麼？看起來好像是HTML中的h1標記的寫法，但中間的又好像是JavaScript的程式碼。這種把HTML寫在JavaScript的程式碼中的技術，稱之為JSX語法，是React中很特別的一種語法，它可以讓你把HTML中的各種標記，直接混在JavaScript程式碼中來寫(並不是字串，而是直接使用)。JSX語法在React中是一種必學的語法。當HTML的標記與JavaScript互相混在一起時，為了要標明與執行JavaScript的程式碼，所以用了花括號({})把程式碼的部份括起來。所以this.props.text這一句是JavaScript的程式碼沒錯。
* Javascript:
  * [ ] Airbnb javascript style https://github.com/airbnb/javascript
  * javacript tutorial https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript
  * 建置React開發環境 https://ithelp.ithome.com.tw/articles/10185954
  * online tools
    * codepen https://codepen.io/
    * codesandbox https://codesandbox.io/s/new

#### 4. cooridnate
* Right ascension 赤經
* Declination 赤緯

## Weekly progress 2018/07/16~2018/07/22
#### 1. study gRPC
* gRPC
  * website: https://grpc.io/
  * github: https://github.com/grpc/grpc
    * install guide: https://github.com/grpc/grpc/blob/master/BUILDING.md
#### 2. frame player
* Frame player: https://www.javascripting.com/view/frame-player
  * A video player without video files, just JSON. Based on 'images frames' thought to mobile devices!
  
#### 3. book for designing new acrh of CARTA
* Patterns of Enterprise Application Architecture, Martin Fowler
  * 3 principle layers
    * Presentation layer - how users interact with SW
    * Domain layer - business logic of this SW in certain specific domain
    * Data source layer - communicatoin with data
* websocket book
  * Getting Started with HTML5 WebSocket Programming
    * HTML5 = Markup language + CSS + Javascript
  * https://legacy.gitbook.com/book/abhirockzz/java-websocket-api-handbook/details
* typescript
  * book https://legacy.gitbook.com/book/zhongsp/typescript-handbook/details
  
#### 4. build Angus's frontend on CentOS
* code: https://github.com/idia-astro/carta-frontend
* build problems in CentOS(solved):
  * emcc需要python2.7.12以上的版本, centOS只有2.7.5, 需update python
    * https://www.jianshu.com/p/5420c4299b40
    * https://www.jianshu.com/p/1babc657914c
    * https://blog.fazero.me/2016/10/13/centos-update-python/
  * jre
    * https://www.digitalocean.com/community/tutorials/how-to-install-java-on-centos-and-fedora
  * cmake 太舊
    * http://jotmynotes.blogspot.com/2016/10/updating-cmake-from-2811-to-362-or.html
  * gcc版本太舊(其實應該是動態library libstdc++.so太舊)
    * 升級gcc & link新的libstdc++.so https://blog.csdn.net/furzoom/article/details/53322510
    * https://blog.csdn.net/zr1076311296/article/details/51334538 
* web assembly related library
  * ast
    * A Library for Handling World Coordinate Systems in Astronomy
    * http://starlink.eao.hawaii.edu/starlink/AST
  * zfp
    * zfp is an open source C/C++ library for compressed numerical arrays that support high throughput read and write random access. zfp also supports streaming compression of integer and floating-point data, e.g., for applications that read and write large data sets to and from disk.
    
#### 5. frontend architecture
* MVC archtitecture
  * MVC模式（Model–view–controller）是軟體工程中的一種軟體架構模式，把軟體系統分為三個基本部分：模型（Model）、視圖（View）和控制器（Controller）。
  * Model(資料模型), View(畫面呈現), Controller(流程控制)
* webassembly
  * wasm_libs: ast, zfp library
  * wasm_src: ast, zfp wrapper
* observer design pattern (key part in MVC)
  * https://en.wikipedia.org/wiki/Observer_pattern
  * https://zh.wikipedia.org/wiki/%E8%A7%82%E5%AF%9F%E8%80%85%E6%A8%A1%E5%BC%8F
  
## Weekly progress 2018/07/09~2018/07/15
#### 1. Trace cpp/desktop
* headers
  * GUI - 捨棄Qt後就可以丟掉不管了
    * CustomWebPage.h // X 沒在用了
    * MainWindow.h
    * DesktopPlatform.h
  * communication - 怎麼切換成uwebsockets
    * NewServerConnector.h
    * SessionDispatcher.h  // cjhsu在這測試uwebsocket
    * NetworkAccessManager.h // X 沒在用了
    * NetworkReplyFileq.h  // X 沒在用了
    * websocketclientwrapper.h  // X 從Qt複製過來, 沒在用了
    * websockettransport.h // X 從Qt複製過來, 沒在用了 Qtwebchannel的websocket
  * grep -rn "websockettransport.h" 看有沒人include, 判斷還有沒有在用
  
#### 2. 小實驗完成(週二前) - 試用uwebsocket, protocol buffer, and combine
* 小實驗: https://github.com/duidae/protobuf-uwebsockets
  * 瀏覽器和後端先經protocol buffer壓縮資料和指令，再透過uwebsockets溝通
  * TODO
    * client javascript version
    * server: how to get websocket payload using uWebSockets?
* websocket介紹: http://www.ruanyifeng.com/blog/2017/05/websocket.html
* websocketd: WebSocket daemon
  * http://websocketd.com/
  * github: https://github.com/joewalnes/websocketd/
  * Full duplex messaging between web browsers and servers
  * Avoid threading headaches
  * 是不可以用這個tool來實現我們的架構?
* libwebsockets:
  * https://github.com/warmcat/libwebsockets
* instruction有沒現成class, parser可用 -> 每一種message就是一種instruction, 所以要定義好多種不一樣的Message(instruction)
  * instruction: name+field
  * cjhsu已定義好, 放在CARTAvis/carta/cpp/CartaLib/Proto
* protocol buffer 淺析
  * serialize https://www.cnblogs.com/royenhome/archive/2010/10/30/1865153.html
* websocket 方法與屬性
  * https://developer.mozilla.org/zh-TW/docs/WebSockets/WebSockets_reference/WebSocket
* socket.io: websocket library between Node.js server/browser
  * https://socket.io/
  
#### 3. Architecture
* server:[CASA libs]+[websocket daemon(thread safe)]+[protobuf encoder] ---------ws---------> client
* backend server development includes
  * develop thread safe websocket daemon
  * connect CASA libs with websocket daemon
  * design protocol buffer for instructions/data
* [TODO] google "socket daemon thread safe"

#### 4. 看desktop怎麼跟Qt連接, 怎麼拆除
* 看哪個版本? release?
  * cjhsu的 cjhsu_Proto
* Qt安裝其他版本
  * 用MaintenanceTool裝要sudo,否則會not enough memory...
  * $ sudo ./MaintenanceTool // MaintenanceTool在/opt/Qt裡面

#### 5. coding IDE
* VS code -> 用這
* Eclipse

#### 6. Collaborative Web App
* https://code.tutsplus.com/tutorials/building-a-collaborative-web-app-with-pubnub-reactjs-and-es6--cms-26565
* https://medium.com/@pvh/pixelpusher-real-time-peer-to-peer-collaboration-with-react-7c7bc8ecbf74
* Github搜尋: collaborative
* Mozilla TogetherJS https://togetherjs.com/
  * TogetherJS is a free, open source JavaScript library by Mozilla that adds collaboration features and tools to your website. By adding TogetherJS to your site, your users can help each other out on a website in real time!
* ShareJS: Collaborative editing in any app
  * https://github.com/josephg/ShareJS
* https://medium.com/front-end-hacking/build-a-collaborative-rich-text-editor-with-node-js-and-socket-io-38ee25b6e315
* 本文简单分析一下这种real time cooperative editing system的设计
  * https://zhuanlan.zhihu.com/p/21844666

## Weekly progress 2018/07/02~2018/07/08
#### 1. Report to ASIAA
* ok

#### 2. Trace carta
* read slack
* read Interface Control Document
* architecture:
  * server ----> RPC/data(protobuf encrytion) ------[uwebsocket]------> browser
  
#### 3. test/integration for uWebSockets, protobuf
* uwebsocket: https://github.com/duidae/uWebSockets-example
* protobuf: https://github.com/duidae/protocol-buffer-example
* uwebsocket+protobuf: 
* uWebSockets: micro websocket document很少也新, 或許可以直接用websocket?
* websocket
  * websocket++(C++): https://www.zaphoyd.com/websocketpp
  * websocket(node.js): https://www.npmjs.com/package/websocket

#### 4. HDF5, Redis study
* [intro to HDF5, Redis](https://chtseng.wordpress.com/2017/08/15/%E5%B7%A8%E9%87%8F%E8%B3%87%E6%96%99%E7%9A%84%E5%A5%BD%E5%A4%A5%E4%BC%B4hdf5-redis/)
* HDF5 https://www.hdfgroup.org/
* redis https://redis.io/

#### 5. possible architecture for reference(於瀏覽器多人協作的功能)
* facebook
* slide.com
* google doc
* github(?)

## Weekly report 2018/06/25~2018/07/01
#### 1. Trace carta
* protobuf
  * Branch: mark/newArch-testProtoBuf
  * use protobuf to transmit .fits file
  * structure of .fits file?
  * [TODO] merge scripts/install_protobuf.sh to scripts/install3party.sh
  * carta/cpp/common_config.pri, testProtoBuf.pro
* entry point for protobuf, uwebsockets
  * carta/cpp
  * 學protobuf把uwebsocket整合進去
  * practice: .fits -> (protobuf encrytion) ------[uwebsocket]-----> (protobuf decryption) -> server
* difference between scrips/buildcasa.sh & Mark's script: cmake flag
  * scrips/buildcasa.sh: 多了-DUseCasacoreNamespace=1
```
cmake -DBoost_NO_BOOST_CMAKE=1 -DCASA_BUILD=1 -DBUILD_TESTING=OFF \
     -DUseCasacoreNamespace=1 \
     -DCMAKE_INSTALL_PREFIX=../../$TARGETOS -DBUILD_PYTHON=1 \
     -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
     -DPYTHON_LIBRARY=/usr/lib64/libpython2.7.so \
     -DWCSLIB_ROOT_DIR=$cartawork/CARTAvis-externals/ThirdParty/wcslib \
     -DCFITSIO_ROOT_DIR=$cartawork/CARTAvis-externals/ThirdParty/cfitsio \
     -DCMAKE_BUILD_TYPE=Release \
     -DCXX11=1 ..
```
#### 2. Qt related
* qmake會根據專案檔（.pro）裡面的資訊自動生成適合平台的 Makefile
* unit Test for Qt
  * http://doc.qt.io/qt-5/qttestlib-tutorial1-example.html
* [TODO]Use Qt creator to build and debug
* update Qt?

#### 3. study docker for mac
* [docker tutorial](https://github.com/twtrubiks/docker-tutorial)
* [如何安裝 Docker for Mac ?](http://oomusou.io/docker/docker-for-mac/)
* [使用 Docker 快速建立測試環境](http://oomusou.io/docker/ubuntu/)

## Weekly report 2018/06/18~2018/06/24
#### 1. Trace & build carta
* [carta builder script from Mark](https://github.com/markccchiang/CARTA-builder)
* startCarta.sh
  * ulimit: 限制shell資源, -n: 限制開啟文件數目
```
ulimit -n 2000
$CARTAWORKHOME/CARTAvis/build/cpp/desktop/CARTA --html $CARTAWORKHOME/CARTAvis/carta/html5/desktop/desktopIndex.html
```
![build](images/2018-06-23%2019-31-45.png)

* release binary
  * CARTA-0.9r-el6-el7/bin/carta.sh <- 啟動點

#### 2. read issues/pull requests
* [protobuf tester](https://github.com/CARTAvis/carta/pull/258)

## Weekly report 2018/06/11~2018/06/17

#### 1. micro web socket study
* [uWebSockets](https://github.com/uNetworking/uWebSockets)
* WebSocket implementation for c++, javascript(Node.js)
* 目前号称最高性能的websocket c++库
* [Comparison of WebSocket implementations](https://en.wikipedia.org/wiki/Comparison_of_WebSocket_implementations)
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
* protobuf install: https://github.com/google/protobuf/blob/master/src/README.md
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
* [Innovation Happens Elsewhere (Version 1.0)](https://www.dreamsongs.com/IHE/)

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
* 整理 scripts/carta.sh 
* [Fix] scripts/carta.sh
  * 53     $dirname/setupcartavis.sh 2>&1  > /dev/null  //should be >/dev/null 2>&1

## CARTA team
* Slack: https://cartaviewer.slack.com/messages/C2S1R8V9P/
* Trello: https://trello.com/b/fViU1U7v/carta-working-group

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

## Open source
* [用Open Source工具開發軟體](http://www.study-area.org/cyril/opentools/opentools/book1.html)
* [Innovation Happens Elsewhere (Version 1.0)](https://www.dreamsongs.com/IHE/)
* [如何貢獻開源專案？](https://shinglyu.github.io/web/2018/05/12/how-to-contribute-to-open-source.html)

## Books:
* lots of free programming books: https://books.goalkicker.com/

## [TODO]
* license study

## Questions
* why not open source CASA directly?
