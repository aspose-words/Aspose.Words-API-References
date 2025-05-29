---
title: WriteProtection.IsWriteProtected
linktitle: IsWriteProtected
articleTitle: IsWriteProtected
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية WriteProtection IsWriteProtected، وتحقق بسهولة مما إذا كانت كلمة مرور حماية الكتابة نشطة لتحسين الأمان وسلامة البيانات.
type: docs
weight: 10
url: /ar/net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

إرجاع`حقيقي` عندما يتم تعيين كلمة مرور لحماية الكتابة.

```csharp
public bool IsWriteProtected { get; }
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
