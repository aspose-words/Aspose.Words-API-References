---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words for .NET
description: 使用 ClearContent 方法轻松清除章节。立即增强您的工作流程并提高内容管理效率！
type: docs
weight: 110
url: /zh/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

清除该部分。

```csharp
public void ClearContent()
```

## 评论

文本[`Body`](../body/)被清除后，只剩下一个代表分节符的空段落。

所有页眉和页脚的文本均被清除，但[`HeaderFooter`](../../headerfooter/)对象本身不会被移除。

## 例子

展示如何清除某个部分的内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// 运行“ClearContent”方法将删除所有部分内容
// 但留下一个空白段落以便再次添加内容。
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
