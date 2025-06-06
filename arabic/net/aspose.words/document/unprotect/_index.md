---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words لـ .NET
description: قم بإلغاء قفل مستنداتك بسهولة باستخدام طريقة إلغاء حماية المستندات لدينا، وإزالة أي حماية بكلمة مرور لتسهيل الوصول والتحرير.
type: docs
weight: 790
url: /ar/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

يزيل الحماية من المستند بغض النظر عن كلمة المرور.

```csharp
public void Unprotect()
```

## ملاحظات

تؤدي هذه الطريقة إلى إلغاء حماية المستند حتى لو كان يحتوي على كلمة مرور للحماية.

لاحظ أن حماية المستندات تختلف عن حماية الكتابة. يتم تحديد حماية الكتابة باستخدام[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

يزيل الحماية من المستند إذا تم تحديد كلمة مرور صحيحة.

```csharp
public bool Unprotect(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لإلغاء حماية المستند بها. |

### قيمة الإرجاع

`حقيقي`إذا تم تحديد كلمة مرور صحيحة وكان المستند غير محمي.

## ملاحظات

تؤدي هذه الطريقة إلى إلغاء حماية المستند فقط إذا تم تحديد كلمة مرور صحيحة.

لاحظ أن حماية المستندات تختلف عن حماية الكتابة. يتم تحديد حماية الكتابة باستخدام[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
