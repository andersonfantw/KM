# ebook KM spec
使用OctoberCMS作為專案主題。

##電子書
將文檔轉為電子書格式。

### A.將office文件轉為pdf
如果是doc,docx,ppt,pptx,xls,xlsx格式的檔案，轉檔成pdf。使用Python的python-docx / XlsxWriter / python-pptx 與ReportLab結合生成pdf。

### B.分析pdf內容，將pdf拆分為單頁，逐頁分析。

a. 若該頁為文字格式的pdf則輸出text-svg。

b. 若該頁為一張圖檔，判斷圖檔內容。若圖檔由色塊組成，輸出svg。

c.若檢查圖檔中是否為統一底色（通常為白底），其他為文字及表格，並包含少量的小圖，則圖檔內容為文件，輸出img2pdf。

d. 若圖檔中檢查顏色變化，考慮圖像中顏色變化的程度，及OCR結果的分析，評估OCR識別出的文字是否分佈在整個圖像中，還是集中在特定區域，作為判斷文字是否覆蓋在複雜背景上的一個依據，輸出mix。

e. 其他則輸出avif。


##知識管理
