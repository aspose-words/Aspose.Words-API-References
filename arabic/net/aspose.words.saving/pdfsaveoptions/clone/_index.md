---
title: PdfSaveOptions.Clone
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions طريقة. إنشاء نسخة عميقة لهذا الكائن.
type: docs
weight: 340
url: /ar/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

إنشاء نسخة عميقة لهذا الكائن.

```csharp
public PdfSaveOptions Clone()
```

### أمثلة

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

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


