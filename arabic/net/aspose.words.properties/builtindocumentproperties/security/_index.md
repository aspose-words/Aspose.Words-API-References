---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة الأمان BuiltInDocumentProperties، التي تُحدد مستوى أمان مستندك بدقة. حسّن حماية مستندك اليوم!
type: docs
weight: 270
url: /ar/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

يحدد مستوى أمان المستند كقيمة رقمية.

```csharp
public DocumentSecurity Security { get; set; }
```

## ملاحظات

استخدم هذه الخاصية لأغراض إعلامية فقط، لأن مايكروسوفت وورد لا يُعيّنها دائمًا. هذه الخاصية متاحة فقط في مستندات DOC وOOXML.

لحماية مستند أو إلغاء حمايته، استخدم [`Protect`](../../../aspose.words/document/protect/) و[`Unprotect`](../../../aspose.words/document/unprotect/) طُرق.

يقوم Aspose.Words بتحديث هذه الخاصية إلى قيمة صحيحة قبل حفظ المستند.

## أمثلة

يوضح كيفية استخدام خصائص المستند لعرض مستوى أمان المستند.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// إذا قمنا بتكوين مستند ليكون للقراءة فقط، فسوف يعرض هذه الحالة باستخدام الخاصية المضمنة "الأمان".
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// قم بحماية المستند ضد الكتابة، ثم تحقق من مستوى الأمان الخاص به.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "الأمان" خاصية وصفية. يُمكننا تعديل قيمتها يدويًا.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### أنظر أيضا

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
