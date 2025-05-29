---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة PdfSaveOptions Clone لإنشاء نسخة طبق الأصل عميقة من كائناتك بسهولة، مما يعزز قدرات إدارة ملفات PDF لديك.
type: docs
weight: 370
url: /ar/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

ينشئ نسخة طبق الأصل عميقة من هذا الكائن.

```csharp
public PdfSaveOptions Clone()
```

## أمثلة

يوضح كيفية تحديث كافة الحقول في مستند فورًا قبل حفظه بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل نصًا باستخدام حقلي PAGE وNUMPAGES. هذه الحقول لا تعرض القيمة الصحيحة في الوقت الفعلي.
// سوف نحتاج إلى تحديثها يدويًا باستخدام طرق التحديث مثل "Field.Update()" و"Document.UpdateFields()"
// في كل مرة نحتاج إليها لعرض القيم الدقيقة.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "UpdateFields" إلى "false" لعدم تحديث كافة الحقول في المستند مباشرة قبل عملية الحفظ.
// هذا هو الخيار المفضل إذا كنا نعلم أن جميع حقولنا ستكون محدثة قبل الحفظ.
// اضبط خاصية "UpdateFields" على "true" لتكرار جميع محتويات المستند
// الحقول وتحديثها قبل حفظها كملف PDF. هذا سيضمن عرض جميع الحقول.
//القيم الأكثر دقة في ملف PDF.
options.UpdateFields = updateFields;

//يمكننا استنساخ كائنات PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
