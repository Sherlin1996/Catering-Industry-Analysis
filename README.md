## Catering Industry Analysis
#### 針對王品、瓦城兩大集團旗下不同類型餐廳，利用爬蟲技術收集在社群媒體上按讚數、文章數，作為聲量以及討論度分析。且能根據個別餐廳，單獨比較客製化分析。
#### 資料來源: Googlemap、ETtody、Dcard、PTT
#### :computer: Data Engineer | Analyst
#### :link: [觀看儀錶板](https://public.tableau.com/views/v4_16551000067390/sheet5?:language=zh-TW&:display_count=n&:origin=viz_share_link)

## :pencil2: Skills
* **Data Visualization :** 
Tableau、Qlick、Python matplotlib
* **DataBase:** 
MySQL
* **Cloud Platform :**
AWS EC2
* **Framwork**
Python Flask

## :pencil2: 分析結果說明
* **王品集團**<br/>
    1.服務-正面評價多次提及服務，代表消費者在餐廳用餐時很重視服務態度</br>
    2.環境-留言提及氣氛、環境、伴侶次數較高，推測店內環境好可被列入適合約會餐廳
* **瓦城集團**<br/>
    1.服務提及次數沒有特別多，表示相較於服務，消費者更注重其他重點<br/>
    2.留言提及冰淇淋、自助吧，推測消費者會因有自助吧而到餐廳消費
* **王品v.s瓦城**<br/>
    1.外送服務-外帶、外送，提及次數高，推測因近兩年受疫情影響，消費者對於這項服務需求提高<br/>
    2.王品正面聲量-服務好、用餐環境佳、好吃、慶生活動多<br/>
    3.王品負面聲量-難定位、候位較久<br/>
    4.瓦城正面聲量-食物、食材、口味佳<br/>
    5.瓦城負面聲量-口味太重、難訂位
 <img width="800" alt="CateringIndustry" src="https://github.com/Sherlin1996/Catering-Industry-Analysis/assets/106952827/d3e6e2b8-5527-4770-bad1-68b44c875595">


## :book: 碰到困難與如何解決

* **資料源收集問題** <br/>
資料源的收集會有 資料太舊，資料量不夠，資訊太雜(圖文不符)、洗評論的問題。
PTT、Dcard兩大論壇的美食版，可以先篩選掉不符合的文章，googlemap評論最直接也最貼近餐廳，
但會有餐廳辦活動促銷的評論收集時透過程式碼先拿掉，ettoday許多企業皆會在他們的網站上下廣告，將其發布新聞的數量當成聲量統計的來源。
* **資料清洗-表情符號**<br/>
googlemap 、Dcard會有表情符號問題，須清洗後再放進資料庫，我們用python emoji、re模組 清洗。
* **資料格式-不一致**<br/>
每個網站抓下來的呈現方式都不同我們需要整理成一致的格式再放進資料庫，舉例:PTT : Thu Jun 2 18:07:01 2022，
Dcard:美食 6月2日 14:38 (今年的文章就不會有年份)，可用 re找到數字、split將數字切開取需要的值、join合併一起、calendar模組 將月份轉換成需要的形式。
