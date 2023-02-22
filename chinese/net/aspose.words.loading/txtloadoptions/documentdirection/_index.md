---
title: TxtLoadOptions.DocumentDirection
second_title: Aspose.Words for .NET API 参考
description: TxtLoadOptions 财产. 获取或设置文档方向 默认值为LeftToRight
type: docs
weight: 30
url: /zh/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

获取或设置文档方向。 默认值为LeftToRight

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

### 例子

显示如何检测纯文本文档的文本方向。

```csharp
// 创建一个“TxtLoadOptions”对象，我们可以将它传递给文档的构造函数
// 修改我们加载纯文本文档的方式。
TxtLoadOptions loadOptions = new TxtLoadOptions();

// 将“DocumentDirection”属性设置为“DocumentDirection.Auto”自动检测
// Aspose.Words 从纯文本加载的每一段文本的方向。
// 每个段落的“Bidi”属性都会存储它的方向。
loadOptions.DocumentDirection = DocumentDirection.Auto;

// 检测从右到左的希伯来语文本。
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// 将英文文本检测为从右到左。
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### 也可以看看

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../txtloadoptions/)
* 部件 [Aspose.Words](../../../)


