---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words لـ .NET
description: SaveOptions UpdateFields ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هيحقيقي  في C#.
type: docs
weight: 160
url: /ar/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تحديث الحقول من أنواع معينة قبل حفظ المستند بتنسيق صفحة ثابت. القيمة الافتراضية لهذه الخاصية هي`حقيقي` .

```csharp
public bool UpdateFields { get; set; }
```

## ملاحظات

يسمح بتحديد ما إذا كان سيتم محاكاة سلوك MS Word أم لا.

## أمثلة

يوضح كيفية تحديث جميع الحقول في المستند مباشرة قبل حفظه في ملف PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل نصًا يحتوي على حقول PAGE وNUMPAGES. لا تعرض هذه الحقول القيمة الصحيحة في الوقت الحقيقي.
// سنحتاج إلى تحديثها يدويًا باستخدام طرق التحديث مثل "Field.Update()" و"Document.UpdateFields()"
// في كل مرة نحتاج إليها لعرض قيم دقيقة.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "UpdateFields" على "خطأ" حتى لا يتم تحديث جميع الحقول في المستند قبل عملية الحفظ مباشرةً.
// هذا هو الخيار المفضل إذا علمنا أن جميع حقولنا ستكون محدثة قبل الحفظ.
// قم بتعيين خاصية "UpdateFields" على "true" للتكرار خلال المستند بالكامل
// الحقول وقم بتحديثها قبل أن نحفظها بصيغة PDF. سيؤدي هذا إلى التأكد من عرض جميع الحقول
// القيم الأكثر دقة في ملف PDF.
options.UpdateFields = updateFields;

// يمكننا استنساخ كائنات PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
