---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words لـ .NET
description: تحكم في سلوك الروابط التشعبية في ملف PDF باستخدام PdfSaveOptions. اضبط الروابط بسهولة لفتحها في نافذة أو علامة تبويب جديدة لتحسين تجربة المستخدم.
type: docs
weight: 230
url: /ar/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

يحصل على قيمة أو يعينها لتحديد ما إذا كانت الروابط التشعبية في مستند Pdf الناتج يجب فتحها في نافذة جديدة (أو علامة تبويب) للمتصفح.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` . عندما يتم تعيين هذه القيمة على`حقيقي` يتم حفظ الارتباطات التشعبية باستخدام كود JavaScript. كود JavaScript هو`app.launchURL("URL"، صحيح)؛` ، حيث`عنوان URL` هو رابط تشعبي.

لاحظ أنه إذا تم تعيين هذا الخيار على`حقيقي` لا يمكن للروابط التشعبية العمل في بعض برامج قراءة ملفات PDF مثل Chrome وFirefox.

تحظر إجراءات JavaScript بموجب التوافق مع PDF/A-1 وPDF/A-2.`خطأ شنيع`سيتم استخدامه تلقائيًا عند الحفظ في PDF/A-1 وPDF/A-2.

## أمثلة

يوضح كيفية حفظ الروابط التشعبية في مستند نقوم بتحويله إلى PDF بحيث تفتح صفحات جديدة عندما نضغط عليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose"، خطأ);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "OpenHyperlinksInNewWindow" على "true" لحفظ جميع الروابط التشعبية باستخدام كود Javascript
// مما يجبر القراء على فتح هذه الروابط في علامات تبويب جديدة في المتصفح/النوافذ.
// قم بضبط الخاصية "OpenHyperlinksInNewWindow" على "false" لحفظ كافة الروابط التشعبية بشكل طبيعي.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
