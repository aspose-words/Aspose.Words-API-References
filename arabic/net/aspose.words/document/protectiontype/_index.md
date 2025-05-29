---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words لـ .NET
description: اكتشف نوع الحماية النشطة للمستندات لتعزيز الأمان وسلامة البيانات. احمِ ملفاتك بسهولة بفضل ميزاتنا المتقدمة.
type: docs
weight: 340
url: /ar/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

يحصل على نوع حماية المستند النشط حاليًا.

```csharp
public ProtectionType ProtectionType { get; }
```

## ملاحظات

تسمح هذه الخاصية باسترجاع نوع حماية المستند الذي تم تعيينه حاليًا. لتغيير نوع حماية المستند، استخدم[`Protect`](../protect/) و[`Unprotect`](../unprotect/) طُرق.

عندما يتم حماية مستند، لا يستطيع المستخدم سوى إجراء تغييرات محدودة، مثل إضافة تعليقات توضيحية، أو إجراء مراجعات، أو استكمال نموذج.

لاحظ أن حماية المستندات تختلف عن حماية الكتابة. يتم تحديد حماية الكتابة باستخدام[`WriteProtection`](../writeprotection/)

## أمثلة

يوضح كيفية حماية مستند وإلغاء حمايته.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// إذا فتحنا هذا المستند باستخدام Microsoft Word بهدف تحريره،
// سوف نحتاج إلى تطبيق كلمة المرور لتجاوز الحماية.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// لاحظ أن الحماية تنطبق فقط على مستخدمي Microsoft Word الذين يفتحون مستندنا.
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

// 2 - مع كلمة المرور الصحيحة:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### أنظر أيضا

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
