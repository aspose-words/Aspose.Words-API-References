---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.SectionLayoutMode 枚举以优化部分布局并增强文档网格行为，从而改善格式控制。
type: docs
weight: 6580
url: /zh/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

指定允许定义文档网格行为的部分的布局模式。

```csharp
public enum SectionLayoutMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Default | `0` | 指定不应将文档网格应用于文档中相应部分的内容。 |
| Grid | `1` | 指定相应部分应在其每一行和每一字符中添加附加行距和字符间距 ，以保持每页的特定行数和每行的特定字符数 。 键入时，字符不会自动与网格线对齐。 |
| LineGrid | `2` | 指定相应部分应为其中的每一行添加额外的行距 ，以保持每页指定的行数。 |
| SnapToChars | `3` | 指定相应部分应在其每行和每字符中添加附加行距和字符间距 ，以保持每页行数和每行字符数的特定值 。 键入时，字符将自动与网格线对齐。 |

## 例子

展示如何指定每行可能包含的字符数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后使用它来设置本节每行的字符数。
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// 字符数也取决于字体的大小。
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

展示如何指定每页行数的限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后使用它来设置本节每页的行数。
// 足够大的字体大小会将一些行推到下一页以避免字符重叠。
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
