---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words لـ .NET
description: حسّن HTML باستخدام خاصية HtmlSaveOptions ExportXhtmlTransitional. تحكّم في إعلانات DOCTYPE لتحسين التوافق مع تنسيقات HTML وMHTML وEPUB.
type: docs
weight: 280
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

يحدد ما إذا كان سيتم كتابة إعلان DOCTYPE عند الحفظ في HTML أو MHTML. عندما`حقيقي` ، يكتب إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هي`خطأ شنيع`. عند الحفظ في EPUB أو HTML5 (Html5 ) يتم دائمًا كتابة إعلان DOCTYPE .

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## ملاحظات

يكتب Aspose.Words دائمًا HTML بشكل جيد بغض النظر عن هذا الإعداد.

متى`حقيقي`، ستبدو بداية مستند الإخراج HTML على النحو التالي:

يهدف Aspose.Words إلى إخراج XHTML وفقًا لمواصفات XHTML 1.0 Transitional، ولكن لا يتوافق الإخراج دائمًا مع DTD. يصعب أو يستحيل ربط بعض الهياكل داخل مستند Microsoft Word مع مستند يتوافق مع مخطط XHTML. على سبيل المثال، لا يسمح XHTML بالقوائم المتداخلة (لا يمكن دمج UL داخل عنصر UL آخر)، ولكن في مستندات Microsoft Word، تكثر القوائم متعددة المستويات.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 انتقالي//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

## أمثلة

يوضح كيفية عرض عنوان DOCTYPE عند تحويل المستندات إلى معيار الانتقال Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// ستحتوي مستندنا فقط على عنوان إعلان DOCTYPE إذا قمنا بتعيين علامة "ExportXhtmlTransitional" إلى "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 انتقالي//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{سطر جديد}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
