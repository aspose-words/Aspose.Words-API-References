---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين قيمة تحدد ما إذا كانت الارتباطات التشعبية الموجودة في ملف PDF الناتج document مفروضة على الفتح في نافذة أو علامة تبويب جديدة من المستعرض.
type: docs
weight: 200
url: /ar/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

الحصول على أو تعيين قيمة تحدد ما إذا كانت الارتباطات التشعبية الموجودة في ملف PDF الناتج document مفروضة على الفتح في نافذة (أو علامة تبويب) جديدة من المستعرض.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خاطئة` . عندما يتم تعيين هذه القيمة على`حقيقي` يتم حفظ الارتباطات التشعبية باستخدام كود JavaScript . كود JavaScript هو`app.ruunchURL ("URL" ، صحيح) ؛`، أين`URL` عبارة عن ارتباط تشعبي.

لاحظ أنه إذا تم تعيين هذا الخيار على`حقيقي` لا يمكن للارتباطات التشعبية work في بعض برامج قراءة PDF مثل Chrome و Firefox .

إجراءات JavaScript محظورة بموجب التوافق مع PDF / A-1 و PDF / A-2.`خاطئة` سيتم استخدامها تلقائيًا عند الحفظ إلى PDF / A-1 و PDF / A-2.

### أمثلة

يوضح كيفية حفظ الارتباطات التشعبية في مستند نقوم بتحويله إلى PDF بحيث يفتحون صفحات جديدة عند النقر فوقها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search؟q=٪20aspose "، خطأ) ;

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "OpenHyperlinksInNewWindow" على "true" لحفظ كافة الارتباطات التشعبية باستخدام كود Javascript
// التي تفرض على القراء فتح هذه الروابط في نوافذ / علامات تبويب متصفح جديدة.
// قم بتعيين خاصية "OpenHyperlinksInNewWindow" على "خطأ" لحفظ كافة الارتباطات التشعبية بشكل طبيعي.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


