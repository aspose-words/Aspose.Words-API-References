---
title: Document.Unprotect
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. يزيل الحماية من المستند بغض النظر عن كلمة المرور.
type: docs
weight: 720
url: /ar/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

يزيل الحماية من المستند بغض النظر عن كلمة المرور.

```csharp
public void Unprotect()
```

### ملاحظات

تقوم هذه الطريقة بإلغاء حماية المستند حتى إذا كان يحتوي على كلمة مرور للحماية.

لاحظ أن حماية المستند تختلف عن الحماية ضد الكتابة. يتم تحديد الحماية ضد الكتابة باستخدام امتداد[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## Unprotect(string) {#unprotect}

يزيل الحماية من المستند إذا تم تحديد كلمة مرور صحيحة.

```csharp
public bool Unprotect(string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| password | String | كلمة المرور لإلغاء حماية المستند باستخدام. |

### قيمة الإرجاع

صواب إذا تم تحديد كلمة مرور صحيحة وكان المستند غير محمي.

### ملاحظات

تقوم هذه الطريقة بإلغاء حماية المستند فقط إذا تم تحديد كلمة مرور صحيحة.

لاحظ أن حماية المستند تختلف عن الحماية ضد الكتابة. يتم تحديد الحماية ضد الكتابة باستخدام امتداد[`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


