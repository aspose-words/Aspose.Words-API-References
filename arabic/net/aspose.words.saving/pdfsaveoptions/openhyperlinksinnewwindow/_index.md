---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد ما إذا كانت الارتباطات التشعبية الموجودة في مستند Pdf الناتج يجب أن يتم فتحها في نافذة أو علامة تبويب جديدة في المتصفح.
type: docs
weight: 230
url: /ar/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

الحصول على أو تعيين قيمة تحدد ما إذا كانت الارتباطات التشعبية الموجودة في مستند Pdf الناتج يجب أن يتم فتحها في نافذة (أو علامة تبويب) جديدة في المتصفح.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع` . عندما يتم ضبط هذه القيمة على`حقيقي` يتم حفظ الارتباطات التشعبية باستخدام كود JavaScript. كود JavaScript هو`app.launchURL("URL"، صحيح)؛` ، أين`عنوان URL` هو ارتباط تشعبي.

لاحظ أنه إذا تم ضبط هذا الخيار على`حقيقي` لا يمكن أن تعمل الارتباطات التشعبية في بعض برامج قراءة PDF، مثل Chrome وFirefox.

إجراءات JavaScript محظورة بموجب التوافق مع PDF/A-1 وPDF/A-2.`خطأ شنيع`سيتم استخدامه تلقائيًا عند الحفظ في PDF/A-1 وPDF/A-2.

### أمثلة

يوضح كيفية حفظ الارتباطات التشعبية في مستند نقوم بتحويله إلى PDF بحيث تفتح صفحات جديدة عندما نضغط عليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose"، false);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين الخاصية "OpenHyperlinksInNewWindow" على "true" لحفظ جميع الارتباطات التشعبية باستخدام كود Javascript
// الذي يجبر القراء على فتح هذه الروابط في علامات تبويب النوافذ/المتصفح الجديدة.
// اضبط الخاصية "OpenHyperlinksInNewWindow" على "خطأ" لحفظ جميع الارتباطات التشعبية بشكل طبيعي.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


