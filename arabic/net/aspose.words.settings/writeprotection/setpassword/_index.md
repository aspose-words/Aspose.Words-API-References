---
title: WriteProtection.SetPassword
linktitle: SetPassword
articleTitle: SetPassword
second_title: Aspose.Words لـ .NET
description: WriteProtection SetPassword طريقة. يضبط كلمة مرور الحماية ضد الكتابة للمستند في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

يضبط كلمة مرور الحماية ضد الكتابة للمستند.

```csharp
public void SetPassword(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لتعيينها. لا يمكن`باطل`، ولكن يمكن أن تكون سلسلة فارغة. |

## ملاحظات

إذا تم تعيين كلمة مرور، فسيطلب Microsoft Word من المستخدم إدخالها أو فتح المستند للقراءة فقط.

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
