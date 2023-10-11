---
title: PageSetup.FirstPageTray
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 获取或设置用于某个部分的第一页的纸盘纸箱 该值特定于实现打印机
type: docs
weight: 130
url: /zh/net/aspose.words/pagesetup/firstpagetray/
---
## PageSetup.FirstPageTray property

获取或设置用于某个部分的第一页的纸盘（纸箱）。 该值特定于实现（打印机）。

```csharp
public int FirstPageTray { get; set; }
```

### 例子

显示如何使文档中的所有部分使用所选打印机的默认纸盒。

```csharp
Document doc = new Document();

// 找到我们将用于打印此文档的默认打印机。
// 您可以使用 PrinterSettings 对象的“PrinterName”属性定义特定的打印机。
PrinterSettings settings = new PrinterSettings();

// 文档中存储的纸盘值是特定于打印机的。
// 这意味着下面的代码将重置所有页面托盘值以使用当前打印机的默认托盘。
// 您可以枚举 PrinterSettings.PaperSources 来查找所选打印机的其他有效纸盘值。
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

显示如何针对不同的纸张尺寸使用不同的打印机纸盘设置打印。

```csharp
Document doc = new Document();

// 找到我们将用于打印此文档的默认打印机。
// 您可以使用 PrinterSettings 对象的“PrinterName”属性定义特定的打印机。
PrinterSettings settings = new PrinterSettings();

// 这是我们将用于“A4”纸张尺寸页面的托盘。
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// 这是我们将用于“Letter”纸张尺寸页面的托盘。
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// 修改本节的PageSettings对象，让Microsoft Word指示打印机
// 根据本节的纸张尺寸使用我们上面确定的纸盘之一。
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
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


