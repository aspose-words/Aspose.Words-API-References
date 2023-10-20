---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions PreserveFormFields ملكية. يحدد ما إذا كان سيتم الاحتفاظ بحقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. الافتراضي هوخطأ شنيع  في C#.
type: docs
weight: 270
url: /ar/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

يحدد ما إذا كان سيتم الاحتفاظ بحقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. الافتراضي هو`خطأ شنيع` .

```csharp
public bool PreserveFormFields { get; set; }
```

## ملاحظات

تتضمن حقول نموذج Microsoft Word إدخال النص والقائمة المنسدلة وعناصر التحكم في خانة الاختيار.

عند التعيين على`خطأ شنيع` ، سيتم تصدير هذه الحقول كنص إلى PDF. عند التعيين على`حقيقي`, سيتم تصدير هذه الحقول كحقول نموذج PDF.

عند تصدير حقول النموذج إلى PDF كحقول نموذج، قد يحدث بعض فقدان التنسيق لأن حقول PDF form لا تدعم جميع ميزات حقول نماذج Microsoft Word.

كما يعتمد حجم الإخراج على حجم المحتوى لأن النماذج القابلة للتحرير في Microsoft Word هي كائنات مضمّنة .

النماذج القابلة للتحرير محظورة بموجب الامتثال لـ PDF/A.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A.

حقول النموذج غير مدعومة عند الحفظ إلى PDF/UA.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق PDF باستخدام طريقة الحفظ وفئة PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربع التحرير والسرد الذي سيسمح للمستخدم باختيار خيار من مجموعة من السلاسل.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// اضبط خاصية "PreserveFormFields" على "true" لحفظ حقول النموذج ككائنات تفاعلية في ملف PDF الناتج.
// اضبط خاصية "PreserveFormFields" على "خطأ" لتجميد كافة حقول النموذج في المستند في
// قيمها الحالية وعرضها كنص عادي في ملف PDF الناتج.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
