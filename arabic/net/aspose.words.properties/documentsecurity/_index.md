---
title: Enum DocumentSecurity
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Properties.DocumentSecurity تعداد. تستخدم كقيمة لـSecurity property. يحدد مستوى الأمان للمستند كقيمة رقمية.
type: docs
weight: 4490
url: /ar/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

تستخدم كقيمة لـ[`Security`](../builtindocumentproperties/security/) property. يحدد مستوى الأمان للمستند كقيمة رقمية.

```csharp
[Flags]
public enum DocumentSecurity
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا توجد حالات أمان محددة بواسطة الخاصية. |
| PasswordProtected | `1` | المستند محمي بكلمة مرور. (لم تظهر الملاحظة في مستند حتى الآن). |
| ReadOnlyRecommended | `2` | المستند الذي سيتم فتحه للقراءة فقط إن أمكن، ولكن يمكن تجاوز الإعداد. |
| ReadOnlyEnforced | `4` | المستند الذي سيتم فتحه دائمًا للقراءة فقط. |
| ReadOnlyExceptAnnotations | `8` | المستند الذي سيتم فتحه دائمًا للقراءة فقط باستثناء التعليقات التوضيحية. |

### أمثلة

يوضح كيفية استخدام خصائص المستند لعرض مستوى أمان المستند.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// إذا قمنا بتكوين مستند ليكون للقراءة فقط، فسوف يعرض هذه الحالة باستخدام خاصية "الأمان" المضمنة.
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// حماية المستند أثناء الكتابة، ثم التحقق من مستوى الأمان الخاص به.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "الأمان" خاصية وصفية. يمكننا تعديل قيمته يدويا.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)


