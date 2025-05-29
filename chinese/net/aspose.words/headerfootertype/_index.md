---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.HeaderFooterType 枚举，轻松识别 Word 文档中的页眉和页脚类型。立即增强您的文档处理能力！
type: docs
weight: 3550
url: /zh/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

标识 Word 文件中的页眉或页脚类型。

```csharp
public enum HeaderFooterType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| HeaderEven | `0` | 偶数页的页眉。 |
| HeaderPrimary | `1` | 主页眉，也用于奇数页。 |
| FooterEven | `2` | 偶数页的页脚。 |
| FooterPrimary | `3` | 主页脚，也用于奇数页。 |
| HeaderFirst | `4` | 该部分第一页的标题。 |
| FooterFirst | `5` | 该部分第一页的页脚。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
