---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ExportXhtmlTransitional ملكية. يحدد ما إذا كان سيتم كتابة إعلان DOCTYPE عند الحفظ في HTML أو MHTML. متىحقيقي  يكتب إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هيخطأ شنيع. عند الحفظ في EPUB أو HTML5 Html5  يتم دائمًا كتابة إعلان DOCTYPE  في C#.
type: docs
weight: 280
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

يحدد ما إذا كان سيتم كتابة إعلان DOCTYPE عند الحفظ في HTML أو MHTML. متى`حقيقي` ، يكتب إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هي`خطأ شنيع`. عند الحفظ في EPUB أو HTML5 (Html5 ) يتم دائمًا كتابة إعلان DOCTYPE .

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## ملاحظات

يقوم Aspose.Words دائمًا بكتابة HTML بشكل جيد بغض النظر عن هذا الإعداد.

متى`حقيقي`، ستبدو بداية مستند إخراج HTML كما يلي:

يهدف Aspose.Words إلى إخراج XHTML وفقًا لمواصفات XHTML 1.0 الانتقالية، ولكن لن يتم التحقق من صحة الإخراج دائمًا مقابل DTD. من الصعب أو من المستحيل تعيين بعض الهياكل الموجودة داخل مستند Microsoft Word إلى مستند سيتم التحقق من صحته مقابل مخطط XHTML. على سبيل المثال، XHTML لا يسمح بالقوائم المتداخلة (لا يمكن دمج UL داخل عنصر UL آخر)، ولكن في مستندات Microsoft Word، تظهر القوائم متعددة المستويات في كثير من الأحيان.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html 
      PUBLIC "-//W3C//DTD XHTML 1.0 الانتقالية//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

## أمثلة

يوضح كيفية عرض عنوان DOCTYPE عند تحويل المستندات إلى المعيار الانتقالي Xhtml 1.0.

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

// ستحتوي وثيقتنا على عنوان إعلان DOCTYPE فقط إذا قمنا بتعيين علامة "ExportXhtmlTransitional" على "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
