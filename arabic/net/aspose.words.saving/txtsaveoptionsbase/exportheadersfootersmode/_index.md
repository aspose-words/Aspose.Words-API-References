---
title: TxtSaveOptionsBase.ExportHeadersFootersMode
second_title: Aspose.Words لمراجع .NET API
description: TxtSaveOptionsBase ملكية. يحدد طريقة تصدير الرؤوس والتذييلات إلى تنسيقات النص. القيمة الافتراضية هيPrimaryOnly .
type: docs
weight: 20
url: /ar/net/aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/
---
## TxtSaveOptionsBase.ExportHeadersFootersMode property

يحدد طريقة تصدير الرؤوس والتذييلات إلى تنسيقات النص. القيمة الافتراضية هيPrimaryOnly .

```csharp
public TxtExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### أمثلة

يوضح كيفية تحديد كيفية تصدير الرؤوس والتذييلات إلى تنسيق نص عادي.

```csharp
Document doc = new Document();

// أدخل الرؤوس / التذييلات الزوجية والأساسية في المستند.
// سيتجاوز الرأس / التذييلات الأساسية الرؤوس / التذييلات الزوجية.
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

// قم بإنشاء كائن "TxtSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند على نص عادي.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// تعيين خاصية "ExportHeadersFootersMode" إلى "TxtExportHeadersFootersMode.None"
// لعدم تصدير أي رؤوس / تذييلات.
// تعيين خاصية "ExportHeadersFootersMode" إلى "TxtExportHeadersFootersMode.PrimaryOnly"
// لتصدير الرؤوس / التذييلات الأساسية فقط.
// تعيين خاصية "ExportHeadersFootersMode" إلى "TxtExportHeadersFootersMode.AllAtEnd"
// لوضع كل الرؤوس والتذييلات لجميع نصوص الأقسام في نهاية المستند.
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

* enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* class [TxtSaveOptionsBase](../)
* مساحة الاسم [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* المجسم [Aspose.Words](../../../)


