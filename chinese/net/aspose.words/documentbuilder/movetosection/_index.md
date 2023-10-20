---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder MoveToSection 方法. 将光标移动到指定节中正文的开头 在 C#.
type: docs
weight: 570
url: /zh/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

将光标移动到指定节中正文的开头。

```csharp
public void MoveToSection(int sectionIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sectionIndex | Int32 | 要移动到的部分的索引。 |

## 评论

什么时候*sectionIndex*大于或等于 0，它指定索引 from 文档的开头，其中 0 是第一个部分。什么时候*sectionIndex*小于 0, 它指定从文档末尾开始的索引，-1 是最后一个部分。

光标移至第一段[`Body`](../../body/)指定部分的。

## 例子

演示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望首页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建标题，然后向文档添加三个页面以显示每种标题类型。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
