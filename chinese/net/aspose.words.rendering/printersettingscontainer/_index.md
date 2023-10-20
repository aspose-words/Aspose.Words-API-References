---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Rendering.PrinterSettingsContainer 班级. 代表一些参数的存储PrinterSettings对象 在 C#.
type: docs
weight: 4580
url: /zh/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

代表一些参数的存储PrinterSettings对象.

要了解更多信息，请访问[以编程方式或使用对话框打印文档](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/)文档文章。

```csharp
public class PrinterSettingsContainer
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | 创建一个容器PrinterSettings. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | 参见PaperSource的DefaultPageSettings. |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | 参见PaperSizes. |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | 参见PaperSources. |

## 评论

访问数据PrinterSettings需要很长时间. `PrinterSettingsContainer`缓存来自的参数PrinterSettings, 因此打印速度更快。

## 例子

演示如何访问并列出打印机的纸张来源和尺寸。

```csharp
// “PrinterSettingsContainer”包含一个“PrinterSettings”对象，
// 其中包含不同打印机驱动程序的唯一数据。
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// “PaperSizes”属性包含指示打印机使用的纸张尺寸列表。
// PrinterSource 和 PrinterSize 都包含“RawKind”属性，
// 相当于 PaperSourceKind 枚举中列出的纸张类型。
// 如果存在与打印页面“RawKind”值相同的纸张来源，
// 打印机将使用提供的纸张来源和尺寸打印页面。
// 否则，打印机将默认使用“DefaultPageSettingsPaperSource”属性指定的源。
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
