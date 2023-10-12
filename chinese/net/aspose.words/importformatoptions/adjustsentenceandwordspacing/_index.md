---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
second_title: Aspose.Words for .NET API 参考
description: ImportFormatOptions 财产. 获取或设置一个布尔值指定是否自动调整句子和单词间距 默认值为错误的.
type: docs
weight: 20
url: /zh/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

获取或设置一个布尔值，指定是否自动调整句子和单词间距。 默认值为`错误的`.

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

### 例子

展示如何自动调整句子和单词间距。

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### 也可以看看

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../importformatoptions/)
* 部件 [Aspose.Words](../../../)


