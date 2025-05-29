---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DocumentDirection 枚举，轻松控制文档中的文本流向。使用这项强大功能，提升文档的可读性和格式！
type: docs
weight: 4030
url: /zh/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

允许指定文档中文本的流动方向。

```csharp
public enum DocumentDirection
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| LeftToRight | `0` | 从左到右的方向。 |
| RightToLeft | `1` | 从右到左的方向。 |
| Auto | `2` | 自动检测方向。 |

## 例子

展示如何检测纯文本文档的文本方向。

```csharp
// 创建一个“TxtLoadOptions”对象，我们可以将其传递给文档的构造函数
// 修改我们加载纯文本文档的方式。
TxtLoadOptions loadOptions = new TxtLoadOptions();

// 将“DocumentDirection”属性设置为“DocumentDirection.Auto”自动检测
// Aspose.Words 从纯文本加载的每个文本段落的方向。
// 每个段落的“Bidi”属性将存储其方向。
loadOptions.DocumentDirection = DocumentDirection.Auto;

// 将希伯来语文本检测为从右到左。
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// 检测英文文本是否从右到左。
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### 也可以看看

* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
