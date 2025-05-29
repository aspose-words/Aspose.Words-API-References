---
title: EditableRange.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية EditableRange Id، وقم بالوصول بسهولة إلى معرفات النطاق القابلة للتحرير وإدارتها لتحسين التحكم في المستندات وزيادة الكفاءة.
type: docs
weight: 40
url: /ar/net/aspose.words/editablerange/id/
---
## EditableRange.Id property

يحصل على معرف النطاق القابل للتحرير.

```csharp
public int Id { get; }
```

## ملاحظات

يجب تحديد المنطقة باستخدام[`EditableRangeStart`](../editablerangestart/) و[`EditableRangeEnd`](../editablerangeend/)

من المفترض أن تكون معرفات النطاق القابلة للتحرير فريدة عبر المستند، ويقوم Aspose.Words تلقائيًا بالحفاظ على معرفات النطاق القابلة للتحرير عند تحميل المستندات وحفظها ودمجها.

## أمثلة

يوضح كيفية العمل مع نطاق قابل للتحرير.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// تسمح لنا النطاقات القابلة للتحرير بترك أجزاء من المستندات المحمية مفتوحة للتحرير.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

//يحتوي النطاق القابل للتحرير ذو التكوين الجيد على عقدة بداية وعقدة نهاية.
// تحتوي هذه العقد على معرفات متطابقة وتشمل عقدًا قابلة للتعديل.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// ترتبط أجزاء مختلفة من النطاق القابل للتحرير ببعضها البعض.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// يمكننا الوصول إلى أنواع العقد لكل جزء كما يلي. النطاق القابل للتحرير ليس عقدة بحد ذاته.
// ولكن كيان يتكون من بداية ونهاية ومحتوياتهما المغلقة.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// إزالة نطاق قابل للتعديل. ستبقى جميع العقد الموجودة داخل النطاق سليمة.
editableRange.Remove();
```

### أنظر أيضا

* class [EditableRange](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
