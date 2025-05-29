---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilder MoveToSection 方法，轻松导航到任何部分主体的开头，提高文档编辑效率。
type: docs
weight: 610
url: /zh/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

将光标移动到指定部分正文的开头。

```csharp
public void MoveToSection(int sectionIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sectionIndex | Int32 | 要移动到的部分的索引。 |

## 评论

什么时候*sectionIndex*大于或等于 0，表示从 开始的索引，其中 0 表示第一部分。当*sectionIndex*小于 0, 它指定了从文档末尾开始的索引，其中 -1 表示最后一节。

光标移动到[`Body`](../../body/)指定部分。

## 例子

展示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望第一页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建页眉，然后向文档添加三页以显示每种页眉类型。
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
