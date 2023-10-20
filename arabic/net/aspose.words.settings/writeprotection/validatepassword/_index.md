---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: Aspose.Words لـ .NET
description: WriteProtection ValidatePassword طريقة. إرجاعحقيقي إذا كانت كلمة المرور المحددة هي نفس كلمة مرور الحماية ضد الكتابة التي تمت حماية المستند بها. إذا لم تكن الوثيقة محمية ضد الكتابة بكلمة مرور فسيتم إرجاعهاخطأ شنيع  في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

إرجاع`حقيقي` إذا كانت كلمة المرور المحددة هي نفس كلمة مرور الحماية ضد الكتابة التي تمت حماية المستند بها. إذا لم تكن الوثيقة محمية ضد الكتابة بكلمة مرور، فسيتم إرجاعها`خطأ شنيع` .

```csharp
public bool ValidatePassword(string password)
```

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

* class [WriteProtection](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
