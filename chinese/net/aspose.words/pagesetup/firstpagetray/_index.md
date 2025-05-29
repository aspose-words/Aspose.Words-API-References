---
title: PageSetup.FirstPageTray
linktitle: FirstPageTray
articleTitle: FirstPageTray
second_title: Aspose.Words for .NET
description: 了解如何使用 PageSetup FirstPageTray 属性自定义首页托盘，以实现最佳打印效果。定制您的打印设置，提升效率！
type: docs
weight: 130
url: /zh/net/aspose.words/pagesetup/firstpagetray/
---
## PageSetup.FirstPageTray property

获取或设置用于部分第一页的纸盘（纸盒）。 该值是特定于实现（打印机）的。

```csharp
public int FirstPageTray { get; set; }
```

## 例子

展示如何让文档中的所有部分使用所选打印机的默认纸盘。

```csharp
Document doc = new Document();

// 查找我们将用于打印该文档的默认打印机。
// 您可以使用 PrinterSettings 对象的“PrinterName”属性定义特定的打印机。
PrinterSettings settings = new PrinterSettings();

// 文档中存储的纸盘值是特定于打印机的。
// 这意味着下面的代码将所有页面托盘值重置为使用当前打印机的默认托盘。
// 您可以枚举 PrinterSettings.PaperSources 来查找所选打印机的其他有效纸盘值。
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

展示如何使用不同的打印机纸盘来设置不同尺寸的纸张进行打印。

```csharp
Document doc = new Document();

// 查找我们将用于打印该文档的默认打印机。
// 您可以使用 PrinterSettings 对象的“PrinterName”属性定义特定的打印机。
PrinterSettings settings = new PrinterSettings();

// 这是我们用于放置“A4”纸张尺寸页面的纸盘。
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// 这是我们用于放置“Letter”纸张尺寸页面的托盘。
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// 修改本节的 PageSettings 对象，让 Microsoft Word 指示打印机
// 根据本节的纸张尺寸，使用我们上面确定的其中一个托盘。
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
