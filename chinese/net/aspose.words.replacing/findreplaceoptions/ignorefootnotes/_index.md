---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 的 IgnoreFootnotes 属性，轻松管理文档中的脚注。使用这个简单的切换功能，提升编辑效率！
type: docs
weight: 90
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

获取或设置一个布尔值，指示是否忽略脚注。 默认值为`错误的`.

```csharp
public bool IgnoreFootnotes { get; set; }
```

## 例子

展示如何在查找和替换操作期间忽略脚注。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// 将“IgnoreFootnotes”标志设置为“true”以获取查找和替换
// 忽略脚注内的文本的操作。
// 将“IgnoreFootnotes”标志设置为“false”以获取查找和替换
// 操作还搜索脚注内的文本。
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
