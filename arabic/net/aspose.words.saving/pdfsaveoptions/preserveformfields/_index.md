---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُبقي خاصية PreserveFormFields في PdfSaveOptions حقول نماذج Microsoft Word في ملفات PDF أو تُحوّلها إلى نص. حسّن جودة مستندك!
type: docs
weight: 280
url: /ar/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

يحدد ما إذا كان سيتم الحفاظ على حقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. الافتراضي هو`خطأ شنيع` .

```csharp
public bool PreserveFormFields { get; set; }
```

## ملاحظات

تتضمن حقول نموذج Microsoft Word إدخال النص وعناصر التحكم في القائمة المنسدلة ومربعات الاختيار.

عند ضبطه على`خطأ شنيع` سيتم تصدير هذه الحقول كنص إلى ملف PDF. عند ضبطها على`حقيقي`سيتم تصدير هذه الحقول كحقول نموذج PDF.

عند تصدير حقول النماذج إلى PDF كحقول نماذج، قد يحدث فقدان لبعض التنسيق لأن حقول PDF form لا تدعم جميع ميزات حقول نماذج Microsoft Word.

بالإضافة إلى ذلك، يعتمد حجم الإخراج على حجم المحتوى لأن النماذج القابلة للتحرير في Microsoft Word هي عبارة عن كائنات مضمنة.

يُحظر استخدام النماذج القابلة للتعديل وفقًا لمعايير PDF/A.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A.

لا يتم دعم حقول النموذج عند الحفظ بتنسيق PDF/UA.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق PDF باستخدام طريقة الحفظ وفئة PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربعًا مركبًا يسمح للمستخدم باختيار خيار من مجموعة من السلاسل.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// قم بتعيين خاصية "PreserveFormFields" إلى "true" لحفظ حقول النموذج ككائنات تفاعلية في ملف PDF الناتج.
// اضبط خاصية "PreserveFormFields" على "false" لتجميد جميع حقول النموذج في المستند عند
//قيمهم الحالية وعرضها كنص عادي في ملف PDF الناتج.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
