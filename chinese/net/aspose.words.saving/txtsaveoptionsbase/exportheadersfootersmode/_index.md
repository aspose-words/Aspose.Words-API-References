---
title: ExportHeadersFootersMode
second_title: Aspose.Words for .NET API 参考
description: 指定页眉和页脚导出为文本格式的方式 默认值为PrimaryOnly.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/
---
## TxtSaveOptionsBase.ExportHeadersFootersMode property

指定页眉和页脚导出为文本格式的方式。 默认值为PrimaryOnly.

```csharp
public TxtExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### 例子

显示如何指定如何将页眉和页脚导出为纯文本格式。

```csharp
Document doc = new Document();

// 将偶数和主要页眉/页脚插入到文档中。
// 主要页眉/页脚将覆盖偶数页眉/页脚。
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// 插入页面以显示这些页眉和页脚。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// 创建一个“TxtSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改我们如何将文档保存为纯文本。
TxtSaveOptions saveOptions = new TxtSaveOptions();

// 将“ExportHeadersFootersMode”属性设置为“TxtExportHeadersFootersMode.None”
// 不导出任何页眉/页脚。
// 将“ExportHeadersFootersMode”属性设置为“TxtExportHeadersFootersMode.PrimaryOnly”
// 仅导出主要页眉/页脚。
// 将“ExportHeadersFootersMode”属性设置为“TxtExportHeadersFootersMode.AllAtEnd”
// 将所有节正文的所有页眉和页脚放在文档的末尾。
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Even header\r\n\r\n" +
                        "Primary header\r\n\r\n" +
                        "Even footer\r\n\r\n" +
                        "Primary footer\r\n\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual("Primary header\r\n" +
                        "Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Primary footer\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n", docText);
        break;
}
```

### 也可以看看

* enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode)
* class [TxtSaveOptionsBase](../../txtsaveoptionsbase)
* 命名空间 [Aspose.Words.Saving](../../txtsaveoptionsbase)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
