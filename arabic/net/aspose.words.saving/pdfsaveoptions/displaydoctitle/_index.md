---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions DisplayDocTitle ملكية. علامة تحدد ما إذا كان شريط عنوان النافذة يجب أن يعرض عنوان المستند المأخوذ من مدخل العنوان في قاموس معلومات المستند في C#.
type: docs
weight: 80
url: /ar/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

علامة تحدد ما إذا كان شريط عنوان النافذة يجب أن يعرض عنوان المستند المأخوذ من مدخل العنوان في قاموس معلومات المستند.

```csharp
public bool DisplayDocTitle { get; set; }
```

## ملاحظات

لو`خطأ شنيع`، يجب أن يعرض شريط العنوان بدلاً من ذلك اسم ملف PDF الذي يحتوي على المستند.

هذه العلامة مطلوبة بموجب التوافق مع PDF/UA.`حقيقي` سيتم استخدام القيمة تلقائيًا عند حفظ إلى PDF/UA.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية عرض عنوان المستند كشريط العنوان.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// اضبط "DisplayDocTitle" على "true" للحصول على بعض برامج قراءة PDF، مثل Adobe Acrobat Pro،
// لعرض قيمة خاصية "العنوان" المضمنة في المستند في علامة التبويب التي تنتمي إلى هذا المستند.
// اضبط "DisplayDocTitle" على "خطأ" لجعل هؤلاء القراء يعرضون اسم ملف المستند.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
