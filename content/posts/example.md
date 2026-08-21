+++
title = 'Override --code-block-bg when using PaperMod as submodule'
date = 2026-08-18T15:10:30+08:00
draft = false
tags = ['Hugo', 'PaperMod']
summary = '關於PaperMod覆蓋css但卻套用不了css樣式的解決方法ˋ'
+++

## 程式碼區塊範例

使用darcula hugo chroma 樣式

```python
def hello_world():
    # 這是一個範例程式碼
    print("Hello, Hugo World!")

    # 進行一些計算
    result = 10 + 20
    return result

if __name__ == "__main__":
    hello_world()
```

可以參考我的檔案範例建立css檔案
我自己是只試過B開頭的css，可以成功套用在paperMod的樣式上
![檔案結構](https://github.com/Shouye0927/ImageBad/raw/main/imgfile_structure.png)

至於為什麼使用c之後的會失敗的原因我猜是hugo在編譯的時候的順序問題，c會在建立code-block這個東西之後才被載入之類的 (我不是很確定)，查AI也沒有一個一定的答案
