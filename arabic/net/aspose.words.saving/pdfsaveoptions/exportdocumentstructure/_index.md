---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words لـ .NET
description: تحكم في بنية تصدير مستندك باستخدام PdfSaveOptions. أدر الإعدادات بسهولة للحصول على أفضل إخراج لملفات PDF، وحسّن كفاءة سير عملك.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم تصدير بنية المستند أم لا.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## ملاحظات

يتم تجاهل هذه القيمة عند الحفظ في PDF/A-1a وPDF/A-2a وPDF/UA-1 لأن بنية المستند مطلوبة لهذا التوافق.

لاحظ أن تصدير بنية المستند يزيد بشكل كبير من استهلاك الذاكرة، وخاصةً للمستندات الكبيرة.

## أمثلة

يوضح كيفية الحفاظ على عناصر بنية المستند، مما قد يساعد في تفسير مستندنا برمجيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// اضبط خاصية "ExportDocumentStructure" على "true" لجعل بنية المستند، مثل هذه العلامات، متاحة عبر
//جزء التنقل "المحتوى" في Adobe Acrobat على حساب زيادة حجم الملف.
// قم بضبط خاصية "ExportDocumentStructure" على "false" لعدم تصدير بنية المستند.
options.ExportDocumentStructure = exportDocumentStructure;

// لنفترض أننا نصدر بنية المستند أثناء حفظه. في هذه الحالة،
// يمكننا فتحه باستخدام Adobe Acrobat والبحث عن علامات للعناصر مثل العنوان
// والفقرة التالية عبر "عرض" -> "إظهار/إخفاء" -> "أجزاء التنقل" -> "العلامات".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
