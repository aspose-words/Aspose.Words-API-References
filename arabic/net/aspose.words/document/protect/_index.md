---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words لـ .NET
description: Document Protect طريقة. يحمي المستند من التغييرات دون تغيير كلمة المرور الحالية أو تعيين كلمة مرور عشوائية في C#.
type: docs
weight: 650
url: /ar/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

يحمي المستند من التغييرات دون تغيير كلمة المرور الحالية أو تعيين كلمة مرور عشوائية.

```csharp
public void Protect(ProtectionType type)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| type | ProtectionType | يحدد نوع الحماية للمستند. |

## ملاحظات

عندما يكون المستند محميًا، يمكن للمستخدم إجراء تغييرات محدودة فقط، مثل إضافة التعليقات التوضيحية، أو إجراء المراجعات، أو إكمال النموذج.

عندما تقوم بحماية مستند، وكان المستند يحتوي بالفعل على كلمة مرور حماية، لا يتم تغيير كلمة مرور الحماية الحالية.

عندما تقوم بحماية مستند، ولا يحتوي المستند على كلمة مرور حماية، تقوم هذه الطريقة بتعيين كلمة مرور عشوائية تجعل من المستحيل إلغاء حماية المستند في Microsoft Word، ولكن لا يزال بإمكانك إلغاء حماية المستند في Aspose.Words لأنه لا تتطلب كلمة مرور عند إلغاء الحماية.

## أمثلة

يوضح كيفية إيقاف الحماية لقسم ما.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// تطبيق الحماية ضد الكتابة على كل قسم في المستند.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// قم بإيقاف تشغيل الحماية ضد الكتابة للقسم الأول.
doc.Sections[0].ProtectedForForms = false;

// في مستند الإخراج هذا، سنكون قادرين على تحرير القسم الأول بحرية،
// ولن نتمكن من تعديل محتويات حقل النموذج إلا في القسم الثاني.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### أنظر أيضا

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

يحمي المستند من التغييرات ويعين كلمة مرور الحماية بشكل اختياري.

```csharp
public void Protect(ProtectionType type, string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| type | ProtectionType | يحدد نوع الحماية للمستند. |
| password | String | كلمة المرور لحماية المستند بها. تحديد`باطل`أو سلسلة فارغة إذا كنت تريد حماية المستند بدون كلمة مرور. |

## ملاحظات

عندما يكون المستند محميًا، يمكن للمستخدم إجراء تغييرات محدودة فقط، مثل إضافة التعليقات التوضيحية، أو إجراء المراجعات، أو إكمال النموذج.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
