---
title: Document.ProtectionType
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يحصل على نوع حماية المستند النشط حاليًا.
type: docs
weight: 310
url: /ar/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

يحصل على نوع حماية المستند النشط حاليًا.

```csharp
public ProtectionType ProtectionType { get; }
```

### ملاحظات

تسمح هذه الخاصية باسترداد نوع حماية المستند المحدد حاليًا[`Protect`](../protect/) و[`Unprotect`](../unprotect/)طُرق.

عندما يكون المستند محميًا ، يمكن للمستخدم إجراء تغييرات محدودة فقط ، مثل إضافة التعليقات التوضيحية أو إجراء المراجعات أو إكمال نموذج.

لاحظ أن حماية المستند تختلف عن الحماية ضد الكتابة. يتم تحديد الحماية ضد الكتابة باستخدام امتداد[`WriteProtection`](../writeprotection/)

### أمثلة

يوضح كيفية حماية مستند وإلغاء حمايته.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// إذا فتحنا هذا المستند مع Microsoft Word يعتزم تحريره ،
// سنحتاج إلى تطبيق كلمة المرور لتجاوز الحماية.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// لاحظ أن الحماية تنطبق فقط على مستخدمي Microsoft Word الذين يفتحون وثيقتنا.
// لم نشفر المستند بأي شكل من الأشكال ، ولسنا بحاجة إلى كلمة المرور لفتحه وتعديله برمجيًا.
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
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


