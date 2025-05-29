---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PdfSaveOptions DisplayDocTitle على تعزيز تجربة PDF الخاصة بك من خلال عرض عناوين المستندات في شريط عنوان Windows لسهولة التعرف عليها.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

علم يحدد ما إذا كان شريط عنوان النافذة يجب أن يعرض عنوان المستند المأخوذ من إدخال العنوان في قاموس معلومات المستند.

```csharp
public bool DisplayDocTitle { get; set; }
```

## ملاحظات

لو`خطأ شنيع`يجب أن يعرض شريط العنوان بدلاً من ذلك اسم ملف PDF الذي يحتوي على المستند.

هذا العلم مطلوب للتوافق مع PDF/UA.`حقيقي` سيتم استخدام القيمة تلقائيًا عند حفظ إلى PDF/UA.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية عرض عنوان المستند كشريط عنوان.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// اضبط "DisplayDocTitle" على "true" للحصول على بعض برامج قراءة ملفات PDF، مثل Adobe Acrobat Pro،
// لعرض قيمة الخاصية المضمنة "العنوان" للمستند في علامة التبويب التي تنتمي إلى هذا المستند.
// قم بضبط "DisplayDocTitle" على "false" لجعل هؤلاء القراء يعرضون اسم ملف المستند.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
