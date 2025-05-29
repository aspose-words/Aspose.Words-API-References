---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words لـ .NET
description: تحكم في أرقام صفحات جدول المحتويات في صيغ HTML وMHTML وEPUB باستخدام خيارات حفظ Html. حسّن تجربة المستخدم وتصفحه بسهولة!
type: docs
weight: 270
url: /ar/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

يحدد ما إذا كان سيتم كتابة أرقام الصفحات في جدول المحتويات عند حفظ HTML وMHTML وEPUB. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## أمثلة

يوضح كيفية عرض أرقام الصفحات عند حفظ مستند يحتوي على جدول محتويات بتنسيق .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج جدول المحتويات، ثم ملء المستند بالفقرات المنسقة باستخدام "العنوان"
// النمط الذي سيختاره جدول المحتويات كمدخلات. سيعرض كل مدخل فقرة العنوان على اليسار.
// ورقم الصفحة التي تحتوي على العنوان على اليمين.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// مستندات HTML لا تحتوي على صفحات. إذا حفظنا هذه الوثيقة بتنسيق HTML،
// لن يكون لأرقام الصفحات التي يعرضها جدول المحتويات لدينا أي معنى.
// عندما نحفظ المستند بتنسيق HTML، يمكننا تمرير كائن SaveOptions لحذف أرقام الصفحات هذه من جدول المحتويات.
// إذا قمنا بتعيين علامة "ExportTocPageNumbers" إلى "true"،
// سيعرض كل إدخال في جدول المحتويات العنوان والفاصل ورقم الصفحة، مع الحفاظ على مظهره في Microsoft Word.
// إذا قمنا بتعيين علامة "ExportTocPageNumbers" إلى "false"،
// ستؤدي عملية الحفظ إلى حذف الفاصل ورقم الصفحة وترك عنوان كل إدخال كما هو.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
