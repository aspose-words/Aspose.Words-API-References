---
title: Class WriteProtection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.WriteProtection فصل. يحدد إعدادات الحماية ضد الكتابة للمستند.
type: docs
weight: 5970
url: /ar/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

يحدد إعدادات الحماية ضد الكتابة للمستند.

لمعرفة المزيد، قم بزيارة[حماية أو تشفير مستند](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) مقالة توثيقية.

```csharp
public class WriteProtection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | إرجاع`حقيقي` عندما يتم تعيين كلمة مرور الحماية ضد الكتابة. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(string) | يضبط كلمة مرور الحماية ضد الكتابة للمستند. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(string) | إرجاع`حقيقي` إذا كانت كلمة المرور المحددة هي نفس كلمة مرور الحماية ضد الكتابة التي تمت حماية المستند بها. إذا لم تكن الوثيقة محمية ضد الكتابة بكلمة مرور، فسيتم إرجاعها`خطأ شنيع` . |

### ملاحظات

تحدد الحماية ضد الكتابة ما إذا كان المؤلف قد أوصى بفتح المستند للقراءة فقط و/أو طلب كلمة مرور لتعديل المستند.

تختلف الحماية ضد الكتابة عن حماية المستندات. تم تحديد الحماية ضد الكتابة في Microsoft Word في خيارات مربع الحوار "حفظ باسم".

لا تقم بإنشاء مثيلات هذه الفئة مباشرة. يمكنك الوصول إلى إعدادات حماية المستندات عبر[`WriteProtection`](../../aspose.words/document/writeprotection/) ملكية.

### أمثلة

يوضح كيفية حماية مستند بكلمة مرور.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// أدخل كلمة مرور يصل طولها إلى 15 حرفًا، ثم تحقق من حالة حماية المستند.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// الحماية لا تمنع تحرير المستند برمجيًا، ولا تقوم بتشفير محتوياته.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


