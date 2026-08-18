+++
title = 'Hugo 技術文章撰寫技巧'
date = 2026-08-18T15:10:30+08:00
draft = false
tags = ['Hugo', '技術文章', '教學']
summary = '這是一篇展示如何在 Hugo PaperMod 中撰寫優質技術文章的範例。'
+++

## 1. 程式碼區塊範例

當你需要展示一段完整的程式邏輯時，Hugo 的 Chroma 系統會自動為你加上高亮與行號（如你的設定）。

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
