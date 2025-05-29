---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Settings.WriteProtection لإدارة إعدادات حماية الكتابة في المستندات بسهولة وتعزيز أمان مستندك.
type: docs
weight: 6800
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
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | إرجاع`حقيقي` عندما يتم تعيين كلمة مرور لحماية الكتابة. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | تعيين كلمة مرور حماية الكتابة للمستند. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | إرجاع`حقيقي` إذا كانت كلمة المرور المحددة هي نفس كلمة مرور الحماية من الكتابة التي تم حماية المستند بها. إذا لم يكن المستند محميًا من الكتابة بكلمة مرور، فيتم إرجاع`خطأ شنيع` . |

## ملاحظات

تحدد حماية الكتابة ما إذا كان المؤلف قد أوصى بفتح المستند للقراءة فقط و/أو يتطلب كلمة مرور لتعديل المستند.

تختلف حماية الكتابة عن حماية المستندات. يتم تحديد حماية الكتابة في Microsoft Word ضمن خيارات مربع حوار "حفظ باسم".

لا تُنشئ مثيلات لهذه الفئة مباشرةً. يمكنك الوصول إلى إعدادات حماية المستندات عبر[`WriteProtection`](../../aspose.words/document/writeprotection/) ملكية.

## أمثلة

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

// الحماية لا تمنع تحرير المستند برمجيًا، ولا تقوم بتشفير المحتويات.
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
