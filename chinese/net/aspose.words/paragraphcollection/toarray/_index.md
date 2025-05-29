---
title: ParagraphCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words for .NET
description: 使用 ToArray 方法轻松地将 ParagraphCollection 转换为数组，从而简化数据管理并增强文档处理。
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

段落数组。

## 例子

展示如何从 NodeCollection 创建数组。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

展示如何在枚举期间使用“热删除”来删除节点。

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
