# Azure 使用心得

### 使用場合
ADL 這門課當中，我只有在作業三（Game Playing）有使用到 Azure 的服務。
所建立的機器依循著助教的投影片所建議，一臺擁有一張 K80 的最低規格虛擬機。
在作業繳交前，總共花了約莫 $68，折合台幣大概為 2000 元。

### 介面（Portal）
介面花了點時間才理解各個物件之間的關聯性，過去在 OpenStack 上操作的經驗可以迅速類比到 Azure 的 dashboard 選項們。
相比於幾年前剛接觸到 Azure 的印象，這一次的操作體驗還不賴，唯查詢 subscription 的餘額有些複雜，需要到 Sponsors 的頁面去實屬困擾。
至今也尚未理解 Directory 跟 Sponsorship 之間的關聯，但除此之外，所有的步驟都有清晰的提示以及 step-by-step 的說明與介紹。

### 評價
虛擬機成功生成以後，剩餘的操作沒有太特殊的地方，反應速度也不賴，在操作這些雲端的虛擬機通常都希望「No news is good news.」
但計費的部份讓我錯愕了些，原來在虛擬機裡頭 `halt -p` 是不夠的，要另外在 dashboard 當中對虛擬機 deallocate、真正將資源釋放掉才會停止計費。
這的計費形式讓我意外的燒掉了剩下的費用，儘管作業寫完後影響不大，但覺得這部分可以更人性化些，像是長時間未使用，可以提供使用者選項允許 Azure 自動 deallocate 資源（deallocate 以後 IP 會換掉，或許可以轉考慮自動寄信提醒使用者這件事情，或是下一次啟動虛擬機的時候，一併提示使用者）。

## 結語
身為學生，使用 Azure 只有一個唯一的目的——無痛完成作業，將精神花在寫作業本身，而非建置環境，Azure 做到了。倘若計價的介面操作與計費說明可以更清晰些，我會更願意掏出信用卡掛些自己的小服務在上面跑。
