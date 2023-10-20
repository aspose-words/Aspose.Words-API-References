---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.TxtExportHeadersFootersMode تعداد. يحدد طريقة تصدير الرؤوس والتذييلات إلى تنسيق نص عادي في C#.
type: docs
weight: 5640
url: /ar/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

يحدد طريقة تصدير الرؤوس والتذييلات إلى تنسيق نص عادي.

```csharp
public enum TxtExportHeadersFootersMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تصدير الرؤوس والتذييلات. |
| PrimaryOnly | `1` | يتم تصدير الرؤوس والتذييلات الأساسية فقط في بداية ونهاية كل قسم. |
| AllAtEnd | `2` | يتم وضع كافة الرؤوس والتذييلات بعد جميع نصوص الأقسام في نهاية المستند. |

## أمثلة

يوضح كيفية تحديد كيفية تصدير الرؤوس والتذييلات إلى تنسيق نص عادي.

```csharp
Document doc = new Document();

// أدخل الرؤوس والتذييلات الزوجية والأساسية في المستند.
// سوف يتجاوز الرأس/التذييلات الأساسية الرؤوس/التذييلات الزوجية.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// أدخل الصفحات لعرض هذه الرؤوس والتذييلات.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// قم بتعيين خاصية "ExportHeadersFootersMode" على "TxtExportHeadersFootersMode.None"
// لعدم تصدير أي رؤوس/تذييلات.
// قم بتعيين خاصية "ExportHeadersFootersMode" على "TxtExportHeadersFootersMode.PrimaryOnly"
// لتصدير الرؤوس/التذييلات الأساسية فقط.
// قم بتعيين خاصية "ExportHeadersFootersMode" على "TxtExportHeadersFootersMode.AllAtEnd"
// لوضع كافة الرؤوس والتذييلات لجميع نصوص الأقسام في نهاية المستند.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
