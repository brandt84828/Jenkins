## 軟體發展生命週期
軟體發展生命週期叫SDLC（Software Development Life Cycle），集合了計畫、開發、測試、部署過程。

![SDLC](/Pictures/SDLC.png)

### 需求分析
第一階段，根據專案需求，團隊執行一個可行性計畫分析，項目需求是公司內部或者客戶提出。這個階段主要是收集資訊，也可能對現有項目進行改善和做一個新專案，還要分析專案的預算和時間，從哪方面收益和佈局。

### 設計
第二階段，系統架構和狀態，要做成什麼樣子，實現什麼功能，創建一個專案計畫，可以用圖表、佈局設計、文案方式呈現。

### 實現
第三階段，專案經理和開發人員配合，開發人員根據任務和設計階段定義進行開發程式，根據專案大小和複雜度，可能需要數月或更長時間來完成。

### 測試
第四階段，測試人員進行測試，包括功能測試、Code測試、壓力測試等。

### 進化
第五階段，對產品進行改進和維護階段，根據使用者的使用回饋，修改功能，bug修復。

## 軟體發展瀑布模型
瀑布模型是最著名和最常使用的軟體發展模型。瀑布模型就是一系列的軟體發展過程。它是由製造業繁衍出來的。一個高度化的結構流程在一個方向上流動，有點像生產線一樣。在瀑布模型創建之初，沒有其它開發的模型，有很多東西全靠開發人員去猜測，去開發。這樣的模型僅適用於那些簡單的軟體發展，但是已經不適合現在的開發了。

![Waterfall](/Pictures/waterfall.png)

|                  優勢                  |                                          劣勢                                          |
| :------------------------------------: | :------------------------------------------------------------------------------------: |
|             簡單易用和理解             |           各個階段的劃分完全固定，階段之間產生大量的文檔，極大地增加了工作量           |
| 當前一階段完成後，只需要去關注後續階段 | 由於開發模型是線性的，使用者只有等到整個過程的末期才能見到開發成果，從而增加了開發風險 |
|     為項目提供按階段劃分的檢查節點     |                                 不適應使用者需求的變化                                 |


## 軟體敏捷開發模型
敏捷開發（Agile Development）的核心是迭代開發（Iterative Development）與增量開發（Incremental Development）。

### 迭代開發
對於大型軟體專案，傳統的開發方式是採用一個大週期（比如一年）進行開發，整個過程就是一次大開發。迭代開發的方式則不一樣，它將開發過程拆分成多個小週期，即一次大開發變成多次小開發，每次小開發都是同樣的流程，所以看上去就好像重複在做同樣的步驟。
舉例來說，SpaceX公司想造一個大推力火箭，將人類送到火星。但是，它不是一開始就造大火箭，而是先造個最簡陋的小火箭Falcon 1。結果，第一次發射就爆炸了，直到第四次發射，才成功進入軌道。然後，開發了中型火箭Falcon 9，九年中發射了70次。最後，才開發Falcon重型火箭。如果SpaceX不採用迭代開發，它可能直到現在還無法上天。

### 增量開發
軟體的每個版本，都會新增一個使用者可以感知的完整功能。也就是說，按照新增功能來劃分迭代。
舉例來說，房產公司開發一個10棟樓的社區。如果採用增量開發的模式，該公司第一個迭代就是交付一棟樓，第二個迭代交付第二棟樓……每個迭代都是完成一棟樓，而不是第一個迭代挖好10棟樓的地基，第二個迭代建好每棟樓的骨架，第三個迭代架設屋頂等。

### 敏捷開發如何迭代
雖然敏捷開發將軟體開發分成多個迭代，但是也要求每次迭代都是一個完整個軟體開發週期，必須按照軟體工程的方法論，進行正規的流程管理。

### 敏捷開發的好處
* 早期交付:
敏捷開發的第一個好處，就是早期交付，從而大大降低成本。
以上一節的房產公司為例，如果按照傳統的瀑布開發模式，先挖10棟樓的地基、再蓋骨架、然後架設屋頂，每個階段都等到前一個階段完成後開始，可能需要兩年才能一次性交付10棟樓。也就是說，如果不考慮預售，該項目必須等到兩年後才能回款。
敏捷開發是六個月後交付第一棟樓，後面每兩個月交付一棟樓。因此，半年就能回款10%，後面每個月都會有現金流，資金壓力就大大減輕了。

* 降低風險:
敏捷開發的第二個好處是，及時瞭解市場需求，降低產品不適用的風險。
請想一想，哪一種情況損失比較小：10棟樓都造好以後，才發現賣不出去，還是造好第一棟樓，就發現賣不出去，從而改進或停建後面9棟樓？

## 持續整合 
持續整合（Continuous Integration，簡稱CI）指的是:頻繁地（一天多次）將Code整合到主幹。
持續整合的目的，就是讓產品可以快速迭代，同時還能保持高品質。它的核心措施是，Code整合到主幹之前必須通過自動化測試。只要有一個測試用例失敗，就不能整合。
通過持續整合，團隊可以快速的從一個功能到另一個功能，簡而言之，敏捷軟體發展很大一部分都要歸功於持續整合。

根據持續整合的設計，Code從提交到生產，整個過程有以下幾步:

* 提交

流程的第一步，是開發者到Code倉庫提交Code。所有後面的步驟都開始於本地Code的一次提交（commit）。

* 測試（第一輪）
  
Code倉庫對commit操作配置了鉤子（hook），只要提交Code或者合併進主幹，就會跑自動化測試。

* 構建

通過第一輪測試，Code就可以合併進主幹，就算可以交付了。
交付後，就先進行構建（build），再進入第二輪測試。所謂構建，指的是將源碼轉換為可以運行的實際Code。比如安裝依賴，配置各種資源（樣式表、JS腳本、圖片）等等。

* 測試（第二輪）

構建完成，就要進行第二輪測試，如果第一輪測試涵蓋了所有內容，第二輪可以省略。

* 部署

過了第二輪測試，當前Code就是一個可以直接部署的版本（artifact）。將這個版本的所有檔打包（tarfilename.tar*）存檔，發到生產伺服器。

* 回滾

一旦當前版本發生問題，就要回滾到上一個版本的構建結果。最簡單的做法就是修改一下符號連結，指向上一個版本的目錄。

###  持續整合的組成要素
* 一個自動構建過程，從檢查Code、編譯構建、運行測試、結果記錄、測試統計等都是自動完成的，無需人工干預
* 一個Code儲存庫，即需要版本控制軟體來保障Code的可維護性，同時作為構建過程的資料庫，一般使用SVN或Git
* 一個持續整合伺服器，Jenkins/gitlab CICD就是一個配置簡單和使用方便的持續整合伺服器


### 持續整合的好處
* 降低風險，由於持續整合不斷去構建，編譯和測試，可以很早期發現問題，所以修復的代價就少
* 對系統健康持續檢查，減少發佈風險帶來的問題
* 減少重複性工作
* 持續部署，提供可部署單元包
* 持續交付可供使用的版本
* 增強團隊信心


## Jenkins介紹
Jenkins是一款流行的開源持續整合（Continuous Integration）工具，廣泛用於專案開發，具有自動化構建測試和部署等功能。

![jenkins](Pictures/jenkinslogo.png)

Jenkins的特色：

* 開源的Java語言開發持續整合工具，支援持續整合，持續部署
* 易於安裝部署配置：可透過yum安裝，或下載war包以及透過docker容器等快速實現安裝部署，可方便web介面配置管理
* 消息通知及測試報告：整合RSS/E-mail通過RSS發佈構建結果，或當構建完成時通過E-mail通知，生成JUnit/TestNG測試報告
* 分散式構建：支援Jenkins能夠讓多台電腦一起構建/測試
* 文件識別：Jenkins能夠跟蹤哪次構建生成哪些jar，哪次構建使用哪個版本的jar等
* 豐富的外掛程式支持：支援擴展外掛程式，可以開發適合自己團隊使用的工具，如git，svn，maven，docker等

## Jenkins安裝和持續整合環境配置

### 持續整合流程說明

![CI Flow](Pictures/CI%20flow.jpg)

1. 首先，開發人員每天進行提交，提交到Git倉庫
2. Jenkins作為持續集成工具，使用Git工具到Git倉庫拉取Code到CI Server，再配合JDK，Maven等軟體完成編譯、測試、審查、打包等工作，在這個過程中每一步出錯，都重新再執行一次整個流程
3. 最後，Jenkins把生成的jar或war包分發到測試伺服器或者生產伺服器，測試人員或使用者就可以存取/訪問


### Server List

| Name                    | IP             | Installed software                                  |
| :---------------------- | :------------- | :-------------------------------------------------- |
| 原始碼託管服務器        | 192.168.66.100 | Gitlab-12.4.2                                       |
| CI Server               | 192.168.66.101 | Jenkins-2.190.3, JDK1.8, Maven3.6.2, Git, SonarQube |
| Application Test Server | 192.168.66.102 | JDK1.8, Tomcat8.5                                   |

### GitLab代碼託管服務安裝
GitLab是一個用於倉庫管理系統的開源專案，使用Git作為代碼管理工具，並在此基礎上搭建起來的web服務。
GitLab和GitHub一樣屬於協力廠商基於Git開發的作品，免費且開源（基於MIT協議），與Github類似，可以註冊使用者並任意提交Code，添加SSHKey等等。不同的是，GitLab是可以部署到自己的伺服器上，資料庫等一切資訊都掌握在自己手上，適合團隊內部協作開發。


#### GitLab安裝
```bash
# 1.安裝相關依賴
yum -y install policycoreutils openssh-server openssh-client postfix

# 2.啟動ssh服務&設置開機啟動
systemctl enable sshd && sudo systemctl start sshd

# 3.設置postfix開機自動啟動，postfix支援gitlab發信功能
systemctl enable postfix && systemctl start postfix

# 4.開啟ssh以及http服務，然後重新加載防火牆列表，如果關閉防火牆就不用作以下配置
firewall-cmd --add-service=ssh --permanent
firewall-cmd --add-service=http --permanent
firewall-cmd --reload

# 5.下載gitlab包並且安裝

# 6.修改gitlab配置，修改gitlab url和port，默認為80
vi /etc/gitlab/gitlab.rb

# 7.重新載入配置和啟動gitlab
gitlab-ctl reconfigure
gitlab-ctl restart

# 8.添加port到防火牆
firewall-cmd --zone=public --add-port=82/tcp --permanent
firewall-cmd --reload
```

#### GitLab create group / user / project
* Create a group

點選Create a group就可以建立一個群組。

* Create a project

進入創建的群組後，再點擊New project創建項目。

* Create a user

點選最上面的Admin Area，再點選Users，就能進入user介面，在這裡可以創建使用者。

* 將使用者加入群組

打開創建的群組，點選左側的Members，找到創建的使用者，後面有權限設置，選擇需要的權限，點選Add to group即可加入。
```
Guest：可以建立issue、發表評論，不能讀寫版本資料
Reporter：可以克隆，不能提交，QA、PM可以賦予這個權限
Developer：可以克隆、開發、提交、push，普通開發者可以賦予這個權限
Maintainer：可以創建項目、添加tag、保護分支、添加成員、編輯，核心開發者可以賦予這個權限
Owner：可以設置訪問權限 - Visibility Level、删除、搬遷、管理成員，開發組組長可以賦予這個權限
```


### Jenkins安裝
```bash
# 1.安裝JDK，安裝目錄為/usr/lib/jvm
yum install java-1.8.0-openjdk* -y

# 2.從Jenkins官網下載安裝檔

# 3.安裝Jenkins

# 4.修改Jenkins配置
vi /etc/sysconfig/jenkins

JENKINS_USER="root"
JENKINS_PORT="8888"

# 5.啟動Jenkins
systemctl start jenkins

# 6.訪問，如有設置防火牆須加入port

# 7.獲取admin密碼並登入
cat /var/lib/jenkins/secrets/initialAdminPassword
```

### Jenkins plugin管理
Jenkins本身不提供很多功能，可以透過使用plugin來滿足使用。例如從Gitlab拉取代碼，使用Maven構建專案等功能需要依靠plugin完成。
自帶的plugin下載是國外的地址，可能會比較慢，可以更換下載地址。

Jenkins->Manage Jenkins->Manage Plugins，點選Available。

這個步驟是把Jenkins官方plugin list下載到本地，接著修改下載位址。
```bash
cd /var/lib/jenkins/updates/
sed -i 's/http:\/\/updates.jenkinsci.org\/download/https:\/\/mirrors.tuna.tsinghua.edu.cn\/jenkins/g' default.json && sed -i 's/http:\/\/www.google.com/https:\/\/www.baidu.com/g' default.json
```
最後Manage plugin點Advanced，把Update Site更改下載地址。
```
修改Update Site為https://mirrors.tuna.tsinghua.edu.cn/jenkins/updates/update-center.json，然後submit並重啟Jenkins服務。

重啟 https://ip:port/restart
```

### Jenkins使用者權限管理
* 安裝Role-based Authorization Strategy plugin : Jenkins可以利用Role-based Authorization Strategy plugin來管理Jenkins使用者。

* 選取Role-Based Strategy : 點選Manage Jenkins -> Configure Global Security，在Authorization中選擇Role-Based Strategy。

* 建立角色 : 點選Manage Jenkins -> Manage and Assign Roles-Manage Role -> Manage Roles
```
Global roles（全域角色）：管理員等高級使用者可以創建基於全域的角色 

Item rols（項目角色）：針對某個或者某些項目的角色

Node roles（節點角色）：節點相關的存取權

在Global roles裡新建一個baseRole的角色，是為了給新使用者分配最基本的Jenkins操作存取權，比如登錄存取權，這邊將baseRole的Overall中的Read打勾。

在Item roles裡新建role1和role2的角色，並指定Pattern(輸入正則表達式)，Pattern是用來表示這個role可以訪問的項目，這裡用project1.*和project2.*來配置，表示role1可以訪問project1前綴的項目，role2可以訪問project2前綴的項目，並把Job的存取權都打勾。

最後記得Save。
```
* 建立使用者 : 點選Manage Jenkins -> Manage Users -> Create User
```
# 建立
Account / Password / Email
qctuser1 / 123456 / qctuser1@qct.io
qctuser2 / 123456 / qctuser2@qct.io
```

* 分配角色 : 點選Manage Jenkins -> Configure Global Security -> Assign Roles
```
將qctuser1 & qctuser2加入Global roles並分配baseRole

將qctuser1 & qctuser2加入Item roles並分別分配role1和role2
```

* 新建Item : 建立兩個項目分別對應project1*和project2*

### Jenkins憑證管理
憑證可以用來儲存密文保護的資料庫密碼、Gitlab密碼、Docker私有倉庫密碼等，以便Jenkins可以和這些第三方應用進行交互。

* 安裝Credentials Binding plugin
* 可以從Manage Jenkins -> Manage Credentials存取
* 在Stores scoped to Jenkins底下點選global，這邊可以新增憑證
```
Username with password：用戶名和密碼

SSH Username with private key： 使用SSH用戶和金鑰

Secret file：需要保密的文字檔，使用時Jenkins會將檔案複製到一個臨時目錄中，再將檔案路徑設置到一個變數中，等構建結束後，所複製的Secret file就會被刪除。

Secret text：需要保存的一個加密的字串，如Github的api token

Certificate：透過上傳證書檔案的方式

常用的憑證類型有：Username with password（使用者密碼）和SSH Username with private key（SSH 金鑰），為了demo，需要下載Git plugin，伺服器上也要安裝Git服務。
```
* 安裝git，jenkins安裝git plugin，jenkins server安裝git
```bash
yum install git -y
```

* (Demo)透過用戶密碼類型拉取code
    1. Manage Jenkins -> Manage Credentials -> global -> Add Credentials
    2. 選擇Username with password，填寫相關資訊
    3. 選擇project -> Genaral中的Source Code Management選擇git輸入Repository url(http)並使用建立的憑證
    4. 點選Bulid Now構建，可以在Console Output看到編譯的訊息
    5. 可以從/var/jenkins_home/workspace/底下路徑找相關project就可以看到拉下來的Code

* (Demo)透過SSH密鑰類型

    ![SSH](/Pictures/SSH.jpg)
    1. 使用root生成公鑰和私鑰
    ```bash
    ssh-keygen -t rsa

    #在/root/.ssh/目錄下保存了公鑰和私鑰
    ```
    2. 把生成的公鑰放在Gitlab中
    3. Manage Jenkins -> Manage Credentials -> global -> Add Credentials
    4. 選擇SSH Username with private key，填寫相關資訊
    5. 選擇project -> Genaral中的Source Code Management選擇git輸入Repository url(ssh)並使用建立的憑證
    6. 點選Bulid Now構建，可以在Console Output看到編譯的訊息
    7. 可以從/var/jenkins_home/workspace/底下路徑找相關project就可以看到拉下來的Code

### Maven安裝和配置

* 安裝Maven
```bash
#下載Maven
wget https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz --no-check-certificate

#解壓縮
tar -zxvf apache-maven-3.8.6-bin.tar.gz -C /opt/maven/

#配置環境變數
vim /etc/profile

#使環境變數生效
source /etc/profile

#測試maven是否安裝成功
mvn -v

#配置文件內容
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk
export MAVEN_HOME=/opt/maven
export PATH=$PATH:$JAVA_HOME/bin:$MAVEN_HOME/bin
```

* 點選Manage Jenkins -> Global Tool Configuration -> JDK -> Add JDK，填入Name和JAVA_HOME的值(取消勾選Install automatically)

* 在下面的Maven也是填入Name和MAVEN_HOME的值(取消勾選Install automatically)

* 加入全域變數，Manage Jenkins -> Config System -> Global properties，點選Apply -> Save
```
JAVA_HOME : /usr/lib/jvm/java-1.8.0-openjdk

MAVEN_HOME : /opt/maven

PATH+EXTRA : $MAVEN_HOME/bin
```

* 測試Maven配置，點選Jenkins的項目 -> 配置，在Add Build Step使用shell，輸入mvn clean package後 -> Build Now即可查看Consloe Output

### Tomcat安裝和配置
* 安裝Tomcat
```bash
# 下載Tomcat
wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.84/bin/apache-tomcat-8.5.84.tar.gz --no-check-certificate

# 解壓縮
tar -zxvf apache-tomcat-8.5.84.tar.gz

# 啟動
cd apache-tomcat-8.5.84/bin/
./startup.sh
#如果訪問不到可以去conf/server.xml更改port
```

* 配置Tomcat角色權限

預設情況下，Tomcat是沒有配置使用者角色，點選manager webapp，會提示403錯誤，但是Jenkins部署到Tomcat，需要用到Tomcat的使用者，所以需要修改Tomcat的tomcat-users.xml配置檔案，建立使用者和存取權限。
```xml
<tomcat-users>
    <role rolename="tomcat"/>
    <role rolename="role1"/>
    <role rolename="manager-script"/>
    <role rolename="manager-gui"/>
    <role rolename="manager-status"/>
    <role rolename="admin-gui"/>
    <role rolename="admin-script"/>
    <user username="tomcat" password="tomcat" roles="manager-gui,manager-script,tomcat,admin-gui,admin-script"/>
</tomcat-users>
```
為了能夠用上述配置登入到Tomcat還需要修改以下配置
```bash
vi /opt/tomcat/webapps/manager/META-INF/context.xml

#註解掉
<!--
<Value className="org.apache.catalina.valves.RemoteAddrValve" allow="xxxxxxx"/>
-->
```

* 重啟Tomcat
```bash
/opt/tomcat/bin/shutdown.sh
/opt/tomcat/bin/startup.sh

訪問http://ip:port/manager/html，輸入tomcat/tomcat
```

### Jenkins構建的項目類型介紹

#### Jenkins構建類型介紹
Jenkins中自動構建類型有很多，常用的有以下三種：
* FreeStyle Project
* Maven Project
* Pipeline Project

每種類型的構建都可以完成一樣的構建過程與結果，只是在操作方式和靈活度等方面有所區別，實際開發的時候可以根據需求和使用習慣選擇。(推薦使用Pipeline Project，靈活度非常高)

#### (Demo)FreeStyle Project
* 創建項目並拉取程式

新建一個FreeStyle Project，從Source Code Management選擇從Git並配置Credentials。

* 編譯打包
在Build裡找到Add build step，選擇"Execute shell"，並輸入以下內容，選擇應用並保存。
```bash
echo "開始編譯和打包"
mvn clean package
echo "編譯和打包結束"
```

* 部屬
    1. Jenkins本身無法實現遠程部屬到Tomcat的功能，需要安裝Deploy to container plugin實現
    2. 添加tomcat使用者憑證
    3. 接著回到FreeStyle Project的配置，找到Post-build Actions，選擇"Deploy war/ear to a container"並填寫。
    ```
    WAR/EAR files : target/*.war
    Containers : Tomcat 8.x Remote，選擇tomcat憑證(沒有需要先新增)，填寫tomcat server url
    ```

#### Maven項目構建
* 安裝Maven Integration Plugin

* 創建Maven項目

* 拉取和部屬的過程和FreeStyle Project相同，只是"構建"的部分不同，在Build裡需要指定pom.xml並設置Maven命令，在Goals and options裡輸入clean package(默認有mvn)。在Post-build Actions裡選擇Deploy war/ear to a container最後保存構建。


#### Pipeline項目構建
* 概念

Pipeline，簡單來說，就是一套運行在Jenkins上的工作流框架，將原來獨立運行於單個或者多個節點的任務連接起來，實現單個任務難以完成的複雜流程編排和視覺化的工作。

* 好處

    * Code：Pipeline以Code的形式實現，通常被檢入原始程式碼控制，使團隊能夠編輯，審查和迭代其傳送流程。
    * 持久：無論是計畫內的還是計畫外的伺服器重啟，Pipeline都是可恢復的。
    * 可停止：Pipeline可接收交互式輸入，以確定是否繼續執行Pipeline。
    * 多功能：Pipeline支援現實世界中複雜的持續整合要求。它支援fork/join、迴圈執行，平行執行任務的功能。
    * 可擴展：Pipeline Plugin支援其DSL的自訂擴展，以及與其他Plugin集成的多個選項。

* 如何創建
    * 使用上要先安裝Pipeline plugin，在新建項目時才會出現選項
    * Pipeline腳本是由Groovy語言實現的，但沒必要單獨去學習Groovy
    * Pipeline支援兩種語法：Declarative（聲明式）和Scripted Pipeline（腳本式）語法
    * Pipeline也有兩種創建方法：可以直接在Jenkins的Web UI介面中輸入腳本；也可以透過創建一個Jenkinsfile指令檔放入項目源碼庫中（一般都推薦在Jenkins中直接從原始程式碼控制（SCM）中直接載入Jenkinsfile Pipeline這種方法）

#### Pipeline語法快速入門(Declarative聲明式-Pipeline)
* 創建Pipeline Project，在Pipeline script，選擇Hello World模板。
```
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
```
聲明式的最外層是pipeline，stages代表整個Pipeline所有的執行階段，通常只有一個stages，裡面包含了多個stage，每個stage代表Pipeline的某個階段，像是拉取Code、編譯構建和部署等。steps代表一個階段內需要執行的邏輯，steps裡是shell腳本，像是git拉取Code和ssh遠程發佈等。

* 一個簡單的聲明式Pipeline例子：
```
pipeline {
    agent any
    stages {
        stage('pull code') {
            steps {
                echo 'pull code'
            }
        }
        stage('build project') {
            steps {
                echo 'build project'
            }
        }
        stage('publish project') {
            steps {
                echo 'publish project'
            }
        }
    }
}
```
可以從Pipeline view去看執行結果，Pipeline view是Pipeline project特有的，它展現執行的過程和時間等，需要安裝Pipeline Stage View plugin。


#### Pipeline語法快速入門(Scripted Pipeline腳本式-Pipeline)
* 創建一個Pipeline Project，Pipeline script中選擇Scripted Pipeline。
```
node {
    def mvnHome
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
        // Get the Maven tool.
        // ** NOTE: This 'M3' Maven tool must be configured
        // **       in the global configuration.
        mvnHome = tool 'M3'
    }
    stage('Build') {
        // Run the maven build
        withEnv(["MVN_HOME=$mvnHome"]) {
            if (isUnix()) {
                sh '"$MVN_HOME/bin/mvn" -Dmaven.test.failure.ignore clean package'
            } else {
                bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/)
            }
        }
    }
    stage('Results') {
        junit '**/target/surefire-reports/TEST-*.xml'
        archiveArtifacts 'target/*.jar'
    }
}
```
1. node代表一個Jenkins節點，Master或者是Agent，是執行Step的具體運行環境，後續在Jenkins的Master-Slave架構會使用。
2. Stage代表一個階段，Pipeline可以劃分多個Stage，每個Stage代表一組操作，像是Build、Test、Deploy，Stage是一個邏輯分組的概念。
3. Step代表一個步驟，是最基本的操作單元，可以是一個Shell命令。
4. 在Pipeline專案裡，有一個Pipeline語法的超連結，點選可以看到有一些常用的Steps，可以選擇對應的範例加上需要的參數，就可以產生Step。

#### Pipeline Script From SCM
在Jenkins裡編寫腳本不方便維護，有另一種方式解決這個問題，把Pipeline Script放到項目裡，用版本控制來跟蹤記錄。
在專案根目錄(建議放在根目錄下)建立一個Jenkinsfile檔，檔案名稱為Jenkinsfile(建議不更動)，將剛才的內容複製進來，提交後到Jenkins執行。
```bash
pipeline {
    agent any

    stages {
        stage('pull code') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'xxxxx', url: 'git url']]])
            }
        }
        stage('build projct') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('deploy project') {
            steps {
                deploy adapters: [tomcat8(credentialsId: 'xxxxx', path: '', url: 'http://x.x.x.x:port')], contextPath: null, war: 'target/*.war'
            }
        }
    }
}
```

### 常用的構建觸發器
Jenkins內建4種建構觸發器 : 
* 觸發遠程構建
* 其他工程構建後觸發(Build after other projects are build)
* 定時構建(Build periodically)
* 輪詢(Poll SCM)

#### 觸發遠程構建
透過remote address觸發，token最好是加密，透過訪問remote address去觸發流程，適合某些系統有時候需要觸發項目時使用。

#### 其他工程構建後觸發
當其他工程構建完成後會觸發此構建。
1. 創建pre_job project
2. 配置需要觸發的工程

#### 定時構建
需要設定定時規則，定時規則表示共有5個值，從左向右分別為：分、時、日、月、周，H代表的是參數(變化的，可以理解為起點)。
```bash
# 每30分鐘構建一次(例如這邊H的意思是從每個小時的30分鐘開始，/表示每隔)
H/30 * * * *

# 每2個小時構建一次
H H/2 * * *

# 每天8時 12時 22時構建(多個時間點中間用逗號隔開)
0 8,12,22 * * *

# 每天中午12點
H 12 * * *

# 每個小時的前半個小時內的每10分鐘
H(0-29)/10 * * * *

# 每兩個小時一次，每個工作日上午9點到下午5點(可能是10:38 12:38 2:38 4: 38)
H H(9-16)/2 * * 1-5
```

#### 輪詢
定時掃描本地原始碼託管服務器的原始碼是否有變更，如果有變更就觸發項目構建。系統開銷較大，不建議使用。

### Git hook自動觸發構建
輪詢SCM可以實現Gitlab更新後項目自動構建，但是輪詢SCM的性能不佳。另一種方法是利用GitLab的webhook來實現push後立即觸發項目構建。

* 輪詢SCM原理：Jenkins定時發送請求查看Gitlab有無變動
* webhook原理：GitLab變動後發送構建請求給Jenkins

#### 使用步驟
1. 安裝Gitlab Plugin
2. Jenkins設置自動構建 : 在Build Triggers就能看到新安裝的gitlab hook，選擇此選項
3. GitLab配置webhook : 先用管理者登入GitLab，開啟相關功能。Admin Area -> Settings -> Network，選取"Allow requests to the local network from web hooks and services"
4. 給專案添加webhook，點選專案 -> Settings -> Webhooks，輸入從Jenkins取得的webhook Url(可以先用gitlab test進行測試)
5. 在Jenkins開放外部認證功能 : Manage Jenkins -> Configure System，取消"Enable authentication for '/project' end-point"
6. 設置完成，之後即可透過gitlab hook自動構建

 
### Jenkins的參數化構建
有時在項目構建的過程中，需要根據使用者的輸入動態傳入參數，從而影響整個構建結果，這時就可以使用參數化構建。

#### (Demo)項目創建分支並推送到Gitlab上
1. 在構建配置中找到"This project is parameterized"並勾選，選擇String parameter，Name設定為branch，Default設為master
2. 這時在項目內左邊會多一個"Build with Parameters"，點選後就可以輸入參數，但使用前須先修改腳本的寫法
3. 將腳本中stage為pull code的區塊內的master更改為${branch}，然後將此Jenkinsfile上傳至Gitlab
4. 在專案中加入其他分支
5. 在Build with Parameters輸入對應的分支並構建

### 設置Mail Server發送構建結果
* 安裝Email Extension Template Plugin(加強原本Extension功能，提供模板)
* 設置Mail相關參數，Manage Jenkins -> Configure System(Jenkins Location & Extended Email Notification & Email Notification)
* 配置完成可以點選Test 
* 準備郵件內容，在項目根目錄下編寫email.html並push到Gitlab，變數可以從Manage Jenkins -> Configure System中的"Content Token Reference"查詢，點擊右邊的"?"可以展開細節
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>$PROJECT_NAME - Build # $BUILD_NUMBER </title>
</head>

<body leftmargin ="8" maginwidth="0" topmargin="8" marginheight="4"
      offset="0">
<div>
    <table width="100%" cellpadding="0" cellspacing="0"
           style="font-size: 11pt; font-family: Tahoma, Arial, Helvetica, sans-serif">
        <tr>
            <td>(本郵件由Jenkins自動發送，請勿回覆！)</td>
        </tr>
        <tr>
            <td>
                <h2> <font color="#0000FF">Result -${BUILD_STATUS}</font> </h2></td>
        </tr>
        <tr>
            <td>
                <br /><b><font color="#0B610B">Info</font></b>
                <hr size="2" width="100%" align="center" />
            </td>
        </tr>
        <tr>
            <td>
                <ul>
                    <!--li>詳細測試報告 ：<a href="${PROJECT_URL}ws/target/jmeter/html">${PROJECT_URL}target/jmeter/html</a></li-->
                    <li>項目名稱 ：系統檢查</li>
                    <li>構建編號 ：第${BUILD_NUMBER}次構建</li>
                    <li>觸發原因 ：${CAUSE}</li>
                    <li>構建日誌 ：<a href="${BUILD_URL}console">${BUILD_URL}console</a></li>
                    <li>構建 Url ：<a href="${BUILD_URL}">${BUILD_URL}</a></li>
                    <li>工作目錄 : <a href="${PROJECT_URL}ws">${PROJECT_URL}ws</a></li>
                    <li>項目 Url ：<a href="${PROJECT_URL}">${PROJECT_URL}</a></li>
                    <li>歷史變更記錄 ：<a href="${PROJECT_URL}changes">${PROJECT_URL}changes</a></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>
                <br /> <b><font color="#0B610B">詳細報告請查閱附件(報告記錄了介面的詳細請求和回應)</font></b>
            </td>
        </tr>
        <tr>
            <td>
                <br /> <b><font color="#0B610B">匯總報告如下:</font></b>
                <hr size="4" width="100%" align="center" />
            </td>
        </tr>
        <tr>
            <td colspan="2" align="center">
                <div>${FILE,path="html/TestReport${BUILD_TIMESTAMP}.html"}</div>
            </td>
        </tr>
    </table>
</div>
</body>
</html>
```
* 修改腳本，關於post語法可以從Pipeline Syntax -> Declarative Directive Generator中查詢，選擇"post: Post Stage or Build Conditions"並根據條件產生對應的語法。郵件內容則選擇"emailext: Extended Email"產生。
```bash
pipeline {
    agent any

    stages {
        stage('pull code') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'xxx', url: 'git url']]])
            }
        }
        stage('build projct') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('deploy project') {
            steps {
                deploy adapters: [tomcat8(credentialsId: 'xxxxx', path: '', url: 'url')], contextPath: null, war: 'target/*.war'
            }
        }
    }
    post {
        always {
            emailext(
                subject: 'Notification：${PROJECT_NAME} - Build # ${BUILD_NUMBER} - ${BUILD_STATUS}!',
                body: '${FILE,path="email.html"}',
                to: 'receiver'
            )
        }
    }
}
```

## SonarQube程式碼檢測平台
SonarQube是一個用於管理程式碼品質的開源平台，可以快速的定位程式碼中潛在或明顯的錯誤。

### 安裝SonarQube
1. 安裝MySQL/Postgrel SQL(新版已不支援MySQL)
2. 安裝SonarQube(可用docker & k8s)

### Jenkins + SonarQube實現原始碼審查
![JenkinsToSonarQubeFlow](/Pictures/JenkinsToSonarQubeFlow.jpg)

* 安裝SonarQube Scanner Plugin
* 新增一個Scanner : Manage Jenkins -> Global Tool Configuration -> SonarQube Scanner，新增一個SonarQube Scanner。
* 新增一個SonarQube Server : Manage Jenkins -> Configure System -> SonarQube servers，新增一個SonarQube Server。
* 添加SonarQube憑證 : Manage Jenkins -> Manage Credentials -> Stores scoped to Jenkins-global，新增一個Secret text，然後把從SonarQube取得的token加入。

### 非Pipeline項目
* 在Build內增加構建步驟，點選Execute SonarQube Scanner。
```bash
Task to run : scan

#兩種選擇一種，看是要以檔案的方式提供或是直接寫在Jenkins上，參考下方內容
Path to project properties || Analysis properties
```
* 內容
```bash
# must be unique in a given SonarQube instance
# 這裡的web_demo需要換成自己的專案名
sonar.projectKey=web_demo
# this is the name and version displayed in the SonarQube UI. Was mandatory
prior to SonarQube 6.1.
sonar.projectName=web_demo #寫自己的專案名稱
sonar.projectVersion=1.0
# Path is relative to the sonar-project.properties file. Replace "\" by "/" on
Windows.
# This property is optional if sonar.modules is set.
sonar.sources=. #掃描的路徑，ex:/src/**
sonar.exclusions=**/test/**,**/target/** #排除的路徑
sonar.java.source=1.8
sonar.java.target=1.8
sonar.java.binaries=./target/classes
# Encoding of the source code. Default is default system encoding
sonar.sourceEncoding=UTF-8
```

* 構建完成後可以到SonarQube查看結果。

### Pipeline項目
* 產生一個sonar-project.properties
```bash
# must be unique in a given SonarQube instance
# 這裡的web_demo需要換成自己的專案名
sonar.projectKey=web_demo
# this is the name and version displayed in the SonarQube UI. Was mandatory
prior to SonarQube 6.1.
sonar.projectName=web_demo #寫自己的專案名稱
sonar.projectVersion=1.0
# Path is relative to the sonar-project.properties file. Replace "\" by "/" on
Windows.
# This property is optional if sonar.modules is set.
sonar.sources=. #掃描的路徑，ex:/src/**
sonar.exclusions=**/test/**,**/target/** #排除的路徑
sonar.java.source=1.8
sonar.java.target=1.8
sonar.java.binaries=./target/classes
# Encoding of the source code. Default is default system encoding
sonar.sourceEncoding=UTF-8
```

* 在Jenkinsfile內加入
```
stage('Code checking') {
    steps{

        script {
        	// 引入Scanner工具，SonarQube Scanner與Global Tool Configuration -> SonarQube Scanner裡的設置要相同
            scannerHome = tool 'sonar-scanner'
        }
        // 引入Server env，要與Configure System -> SonarQube servers裡的Name相同
        withSonarQubeEnv('sonarqube') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
```

* 構建完成後可以到SonarQube查看結果。


## Plugin

### Publish Over SSH
* 安裝Publish Over SSH Plugin
* 去Manage Jenkins -> Configure System中進行設置
```bash
參數說明
Passphrase：SSH的密碼
* 使用用戶名/密碼登錄時的密碼
* 使用私鑰登錄時為私鑰的密碼

Path to key：
SSH私鑰的檔案路徑，路徑可以是絕對路徑，也可以是相對$JENKINS_HOME的相對路徑

Key：私鑰檔案的內容

如果"Key"和"Path to key"都設置，則"Key"的優先順序較高，私鑰的密碼是"Passphrase"中設置的內容。

Disable exec：禁止在目的機上執行命令，勾選後將會忽略在Job配置中"Exec command"選項中設置的命令。
```

* 配置SSH Servers
```bash
參數說明
Name : SSH節點配置的名稱，在Job中使用Publish over SSH Plugin時，此名稱將出現在"SSH Server"中"Name"的下拉清單中。

Hostname : 通過SSH連接到的機器的主機名稱或IP

Username : SSH服務使用的用戶名，使用key進行連接時為key指定的用戶名

Remote Derictory : 遠程機器上真實存在的目錄，並且"Username"指定的使用者要有訪問此目錄的許可權，Plugin將把檔案傳送到此目錄下。
```
* 配置完成即可使用

* 注意事項
```bash
在系統配置的時候會設定Remote Directory，指的是遠端主機的目錄，這會與後續在Project設定的Remote Directory互相配合。
最後的遠端路徑 = 系統配置的Remote Directory + 建置時配置的Remote Directory
 
在建置時配置時，Source相對路徑問題，為var/jenkins_home/workspace/[project]/
舉例：
如果/var/lib/jenkins/workspace/projectA/md/xx.md的話，在下面source file中只要寫md/xx.md

如果不去首碼，上面的例子會在遠端目錄上生成如下目錄/remote directory/md/xx.md，而需要的只有md檔，所以透過remove prefix選項可以把md/去掉，只取得md檔。
```


## Reference
[GitLab Docs](https://docs.gitlab.com/ee/)

[Jenkins](https://www.jenkins.io/download/)

[SonarQube](https://www.sonarqube.org/)