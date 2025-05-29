---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words لـ .NET
description: أمّن مستنداتك بسهولة مع Document Protect. امنع التغييرات غير المصرح بها مع الحفاظ على كلمة مرورك الحالية سليمة أو استخدام كلمة مرور عشوائية.
type: docs
weight: 690
url: /ar/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

يحمي المستند من التغييرات دون تغيير كلمة المرور الموجودة أو تعيين كلمة مرور عشوائية.

```csharp
public void Protect(ProtectionType type)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| type | ProtectionType | يحدد نوع الحماية للمستند. |

## ملاحظات

عندما يتم حماية مستند، لا يستطيع المستخدم سوى إجراء تغييرات محدودة، مثل إضافة تعليقات توضيحية، أو إجراء مراجعات، أو استكمال نموذج.

عندما تقوم بحماية مستند، والمستند يحتوي بالفعل على كلمة مرور حماية، فإن كلمة مرور الحماية الموجودة لا تتغير.

عندما تقوم بحماية مستند، والمستند ليس لديه كلمة مرور حماية، تقوم هذه الطريقة بتعيين كلمة مرور عشوائية تجعل من المستحيل إلغاء حماية المستند في Microsoft Word، ولكن لا يزال بإمكانك إلغاء حماية المستند في Aspose.Words لأنه لا يتطلب كلمة مرور عند إلغاء الحماية.

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

// في وثيقة الإخراج هذه، سنكون قادرين على تحرير القسم الأول بحرية،
// ولن نتمكن من تحرير محتويات حقل النموذج إلا في القسم الثاني.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### أنظر أيضا

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

يحمي المستند من التغييرات ويحدد بشكل اختياري كلمة مرور للحماية.

```csharp
public void Protect(ProtectionType type, string password)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| type | ProtectionType | يحدد نوع الحماية للمستند. |
| password | String | كلمة المرور لحماية المستند باستخدام. حدد`باطل` أو سلسلة فارغة إذا كنت تريد حماية المستند بدون كلمة مرور. |

## ملاحظات

عندما يتم حماية مستند، لا يستطيع المستخدم سوى إجراء تغييرات محدودة، مثل إضافة تعليقات توضيحية، أو إجراء مراجعات، أو استكمال نموذج.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
