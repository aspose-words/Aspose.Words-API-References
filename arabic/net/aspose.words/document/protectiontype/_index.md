---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words لـ .NET
description: Document ProtectionType ملكية. للحصول على نوع حماية المستند النشط حاليًا في C#.
type: docs
weight: 330
url: /ar/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

للحصول على نوع حماية المستند النشط حاليًا.

```csharp
public ProtectionType ProtectionType { get; }
```

## ملاحظات

تسمح هذه الخاصية باسترداد نوع حماية المستند المحدد حاليًا. لتغيير نوع حماية المستند، استخدم[`Protect`](../protect/) و[`Unprotect`](../unprotect/) طُرق.

عندما يكون المستند محميًا، يمكن للمستخدم إجراء تغييرات محدودة فقط، مثل إضافة التعليقات التوضيحية، أو إجراء المراجعات، أو إكمال النموذج.

لاحظ أن حماية المستند تختلف عن الحماية ضد الكتابة. يتم تحديد الحماية ضد الكتابة باستخدام[`WriteProtection`](../writeprotection/)

## أمثلة

يوضح كيفية حماية مستند وإلغاء حمايته.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// إذا فتحنا هذا المستند باستخدام برنامج Microsoft Word بهدف تعديله،
// سنحتاج إلى تطبيق كلمة المرور لتجاوز الحماية.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// لاحظ أن الحماية تنطبق فقط على مستخدمي Microsoft Word الذين يفتحون وثيقتنا.
// لم نقم بتشفير المستند بأي شكل من الأشكال، ولا نحتاج إلى كلمة المرور لفتحه وتحريره برمجيًا.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// هناك طريقتان لإزالة الحماية من المستند.
// 1 - بدون كلمة مرور:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - بكلمة المرور الصحيحة:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### أنظر أيضا

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
