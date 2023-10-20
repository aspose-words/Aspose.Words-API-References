---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: 用于 .NET 的 Aspose.Words
description: ListLevel CustomNumberStyleFormat 财产. 获取此列表级别的自定义数字样式格式例如a ç ĝ  在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

获取此列表级别的自定义数字样式格式。例如：“a, ç, ĝ, ...”.

```csharp
public string CustomNumberStyleFormat { get; }
```

## 例子

显示如何获取具有自定义编号样式的列表的格式。

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// 我们可以获取列表项的指定索引的值。
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### 也可以看看

* class [ListLevel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
