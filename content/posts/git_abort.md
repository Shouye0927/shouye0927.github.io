+++
date = '2026-09-09T19:04:32+08:00'
draft = false
title = 'Git 基礎知識'
+++

![Git 3大區塊](https://cdn.jsdelivr.net/gh/Shouye0927/ImageBad@main/img/gitBasic.png)
圖中可以看到git分為三個區塊，**`Working directory`**、**`Staging Area`**、**`Repository`**，而在使用git的時候，**`git add`** 就是將目前尚未加入staging area 的變更放進去、**`git commit`** 就是能夠將目前staging area中所做的變更給他個編號，讓他打包成一次紀錄放進repo中

### git add 和 git commit

> 如果最終都要commit那甚麼不在working directory中寫好，再一次commit就好，使用git add的意義是甚麼 ?

git add 的核心意義在於讓你能夠選擇性地控制（Staging）哪些修改要打包進下一次的 Commit，而不是把當前工作目錄裡所有的變動全部一股腦塞進去。

例如我正在寫登入功能，卻突然發現主頁面有個bug，如果是還沒寫這篇筆記之前很菜的我，就一次寫完登入功能+修bug，再一次git add .將所有變更加入到staging area就好，但如果事後想要檢查哪個地方修改bug哪個地方修改login那就會造成混亂

那所以我該怎麼做

![git status圖片](https://cdn.jsdelivr.net/gh/Shouye0927/ImageBad@main/img/Screenshot%202026-09-09%20193922.png)

以我正在做的專案為範例，我使用 **`git status`** 檢查目前有變更的檔案有哪些

若我目前Coordinate.tsx中的東西已經寫得差不多，但Component還正在做，我可以先使用 **`git add src/pages/Coordinate.tsx`** 將目前在Coordinate.tsx做得變更給記錄起來，接著輸入 **`git commit -m "調整頁面排版"`** 相關的字眼去讓人瞭解這次得變更主要更改得東西。
