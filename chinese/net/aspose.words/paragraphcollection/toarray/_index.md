---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphCollection ToArray 方法. 将集合中的所有段落复制到新的段落数组中 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

将集合中的所有段落复制到新的段落数组中。

```csharp
public Paragraph[] ToArray()
```

### 返回值

一系列段落。

## 例子

演示如何从 NodeCollection 创建数组。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

演示如何在枚举期间使用“热删除”删除节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// 从枚举中间的集合中删除一个节点。
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### 也可以看看

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
