---
title: TxtSaveOptionsBase.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية TxtSaveOptionsBase ExportHeadersFootersMode تصدير الرأس والتذييل بتنسيقات نصية. الإعداد الافتراضي هو PrimaryOnly.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/
---
## TxtSaveOptionsBase.ExportHeadersFootersMode property

يحدد الطريقة التي يتم بها تصدير الرؤوس والتذييلات إلى تنسيقات النص. القيمة الافتراضية هيPrimaryOnly .

```csharp
public TxtExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## أمثلة

يوضح كيفية تحديد كيفية تصدير الرؤوس والتذييلات إلى تنسيق نص عادي.

```csharp
Document doc = new Document();

// إدراج الرؤوس والتذييلات الزوجية والأساسية في المستند.
// سوف يحل الرأس/التذييل الأساسي محل الرؤوس/التذييلات الزوجية.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

//أدرج الصفحات لعرض هذه الرؤوس والتذييلات.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// اضبط خاصية "ExportHeadersFootersMode" على "TxtExportHeadersFootersMode.None"
// عدم تصدير أي رؤوس/تذييلات.
// اضبط خاصية "ExportHeadersFootersMode" على "TxtExportHeadersFootersMode.PrimaryOnly"
// لتصدير الرؤوس والتذييلات الأساسية فقط.
// اضبط خاصية "ExportHeadersFootersMode" على "TxtExportHeadersFootersMode.AllAtEnd"
// لوضع جميع الرؤوس والتذييلات لجميع نصوص الأقسام في نهاية المستند.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### أنظر أيضا

* enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* class [TxtSaveOptionsBase](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
