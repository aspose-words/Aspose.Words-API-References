---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words لـ .NET
description: Document Unprotect طريقة. إزالة الحماية عن المستند بغض النظر عن كلمة المرور في C#.
type: docs
weight: 740
url: /ar/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

إزالة الحماية عن المستند بغض النظر عن كلمة المرور.

```csharp
public void Unprotect()
```

## ملاحظات

تعمل هذه الطريقة على إلغاء حماية المستند حتى لو كان يحتوي على كلمة مرور حماية.

لاحظ أن حماية المستند تختلف عن الحماية ضد الكتابة. يتم تحديد الحماية ضد الكتابة باستخدام[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

إزالة الحماية عن المستند إذا تم تحديد كلمة مرور صحيحة.

```csharp
public bool Unprotect(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لإلغاء حماية المستند بها. |

### قيمة الإرجاع

`حقيقي` إذا تم تحديد كلمة مرور صحيحة وكان المستند غير محمي.

## ملاحظات

تعمل هذه الطريقة على إلغاء حماية المستند فقط في حالة تحديد كلمة مرور صحيحة.

لاحظ أن حماية المستند تختلف عن الحماية ضد الكتابة. يتم تحديد الحماية ضد الكتابة باستخدام[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
