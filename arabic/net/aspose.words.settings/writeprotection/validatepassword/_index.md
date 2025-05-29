---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: Aspose.Words لـ .NET
description: أمّن مستنداتك باستخدام طريقة WriteProtection ValidatePassword. تحقق بسهولة من تطابق كلمة المرور مع حماية المستند لتعزيز الأمان.
type: docs
weight: 40
url: /ar/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

إرجاع`حقيقي` إذا كانت كلمة المرور المحددة هي نفس كلمة مرور الحماية من الكتابة التي تم حماية المستند بها. إذا لم يكن المستند محميًا من الكتابة بكلمة مرور، فيتم إرجاع`خطأ شنيع` .

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

* class [WriteProtection](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
