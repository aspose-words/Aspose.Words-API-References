---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.SectionLayoutMode 枚举. 指定允许定义文档网格行为的部分的布局模式 在 C#.
type: docs
weight: 5750
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
| Default | `0` | 指定文档网格不应应用于文档中相应部分的内容。 |
| Grid | `1` | 指定相应部分应将附加行间距和字符间距 添加到其中的每一行和字符，以保持每页的特定行数 和每行字符数。 字符不会自动与网格线对齐打字. |
| LineGrid | `2` | 指定相应部分应向其内的每一行添加额外的行间距 ，以保持每页指定的行数。 |
| SnapToChars | `3` | 指定相应部分应将附加行间距和字符间距 添加到其中的每一行和字符，以便保持每页的特定行数和每行字符数。 键入时字符将自动与网格线对齐。 |

## 例子

演示如何指定每行可以包含的字符数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后用它来设置此部分中每行的字符数。
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// 字符数还取决于字体的大小。
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

演示如何指定每页可以拥有的行数限制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 启用间距，然后用它来设置此部分中每页的行数。
// 足够大的字体大小会将某些行向下推到下一页，以避免字符重叠。
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
