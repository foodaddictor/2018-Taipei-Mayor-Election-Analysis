# 2018-Taipei-Mayor-Election-Analysis
This is a simple analysis of Taipei mayor election which can gives you a quick overview and some statistics result of 2018 election in Taiwan.

本說明所有函數皆以中括號表示，如「function_name」。且所有圖表皆以大安區為例。
執行此專案需要的相關套件有:pandas, matplolib.pyplot, BeautifulSoup, requests, seaborn, time 
需要的檔案有:台北市行政區人口.xlsx

一、	函數
此專案一共設計3個函數分別為「taipei_votes_result」、「get_votes_data」、「taipei_votes_results」。
1.	taipei_votes_result
參數: district_name
功能: 輸入臺北市行政區中文名稱後，函數會自動到中央選舉委員會的網站根據中文名稱對應的代碼，將2018臺北市市長選舉結果爬取下來，並且儲存名為”votes_result”的data.frame物件。
2.	get_votes_data
參數: 無
功能: 有別於「taipei_votes_results」函數，此函數直接將臺北市所有行政區2018市長選舉票數結果抓取下來，並且儲存名為”votes_data”的data.frame物件。
3.	taipei_votes_results
參數: 無
功能:
參考106年臺北市所得收入者每人年所得從小排到大整理成data.frame，名稱為”dis_income”，如圖1為例，並且以長條圖呈現如圖4左上。
利用「get_votes_data」得到的所有候選人各行政區的得票數，以折現圖呈現，如圖4左下。
印出”請輸入一個行政區名稱:”，根據使用者輸入的臺北市行政區名稱利用「taipei_votes_result」將此行政區的票數結果以data.frame及常條圖印出，分別如圖3及圖4右下。
再將「106年12月底臺北市各行政區按性別、年齡分統計表」excel檔案匯入進行資料的清理，整理從20歲到89歲，每10歲為截距，並且以使用者輸入的行政區，將性別及行政區做出年齡分佈的data.frame以及長條圖，分別如圖2及圖4右上為例。

二、	專案結果
1.	人口年齡及所得分佈
由圖4可看出，大安區屬於臺北市年均所得第二高的行政區，但幾乎跟第一名的松山差不多。年齡人口集中於40~59歲區間，30~39歲與60~69歲人口差不多。
2.	選舉結果
由圖4可看出，臺北市長票數主要集中於2號的丁守中以及4號的柯文哲，但丁守中的票數又明顯高於柯文哲大約1萬票，且由折線圖也可明顯看出大安區及文山區都是丁守中票數相較於其他行政區大贏柯文哲的票倉。

三、	結論
此專案所呈現的圖表皆不帶有作者主觀解釋上的意義，同樣的結果對於不同的人皆有不同的詮釋方式，再進行更深入的分析時必須考慮到一些假設，例如因為此次投票為匿名投票，是否各年齡層的投票率皆相同?
又例如高年齡人口較多的行政區，如果丁守中以及姚文智的得票率有較高的趨勢相較於其他行政區，能否就代表是敬老金政見的效果?在做相關推論時，我們只能瞭解到統計上的相關性，並不能確保是因果關係。所以在下結論前，是否有更深入的驗證?因此本專案僅提供使用者快速取得及瞭解2018臺北市市長選舉的結果，相關推論皆有待使用者自行詮釋。
