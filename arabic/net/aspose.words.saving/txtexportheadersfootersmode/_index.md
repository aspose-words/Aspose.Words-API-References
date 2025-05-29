---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل TxtExportHeadersFootersMode الخاص بـ Aspose.Words على تعزيز تصدير النص العادي من خلال تخصيص معالجة الرأس والتذييل للحصول على أفضل النتائج.
type: docs
weight: 6440
url: /ar/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

يحدد الطريقة التي يتم بها تصدير الرؤوس والتذييلات إلى تنسيق نص عادي.

```csharp
public enum TxtExportHeadersFootersMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم تصدير الرؤوس والتذييلات. |
| PrimaryOnly | `1` | يتم تصدير الرؤوس والتذييلات الأساسية فقط في بداية ونهاية كل قسم. |
| AllAtEnd | `2` | يتم وضع جميع الرؤوس والتذييلات بعد جميع نصوص الأقسام في نهاية المستند. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
