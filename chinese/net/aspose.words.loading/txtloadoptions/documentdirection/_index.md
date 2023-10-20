---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: 用于 .NET 的 Aspose.Words
description: TxtLoadOptions DocumentDirection 财产. 获取或设置文档方向 默认值为LeftToRight 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

获取或设置文档方向。 默认值为LeftToRight.

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## 例子

演示如何检测纯文本文档文本方向。

```csharp
// 创建一个“TxtLoadOptions”对象，我们可以将其传递给文档的构造函数
// 修改我们加载纯文本文档的方式。
TxtLoadOptions loadOptions = new TxtLoadOptions();

// 设置“DocumentDirection”属性为“DocumentDirection.Auto”自动检测
// Aspose.Words 从纯文本加载的每个文本段落的方向。
// 每个段落的“Bidi”属性将存储其方向。
loadOptions.DocumentDirection = DocumentDirection.Auto;

// 检测希伯来语文本为从右到左。
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// 检测英文文本为从右到左。
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### 也可以看看

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
