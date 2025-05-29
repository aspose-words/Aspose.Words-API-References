---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Settings.MultiplePagesType 枚举，获取高效的文档打印选项。使用灵活的打印设置优化您的工作流程！
type: docs
weight: 6700
url: /zh/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

指定如何打印文档。

```csharp
public enum MultiplePagesType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Normal | `0` | 正常打印，未指定多页。 |
| MirrorMargins | `1` | 在对开页上交换左右边距。 |
| TwoPagesPerSheet | `2` | 每张纸打印两页。 |
| BookFoldPrinting | `3` | 指定是否将文档打印为书本折页。 |
| BookFoldPrintingReverse | `4` | 指定是否将文档打印为反向书本折叠。 |
| Default | `0` | 默认值为Normal |

## 例子

展示如何配置可以打印为书本折页的文档。

```csharp
Document doc = new Document();

// 插入跨越 16 页的文本。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// 配置第一节的“PageSetup”属性，以书本折叠的形式打印文档。
// 当我们双面打印此文档时，我们可以将页面堆叠起来
// 然后将它们全部从中间折叠起来。文档内容将排列成书形折叠。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// 我们只能指定 4 的倍数的纸张数量。
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
