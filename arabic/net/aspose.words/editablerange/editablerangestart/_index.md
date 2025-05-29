---
title: EditableRange.EditableRangeStart
linktitle: EditableRangeStart
articleTitle: EditableRangeStart
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية EditableRangeStart للوصول إلى العقدة التي تُشير إلى بداية نطاقك القابل للتحرير. حسّن تجربة التحرير لديك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words/editablerange/editablerangestart/
---
## EditableRange.EditableRangeStart property

يحصل على العقدة التي تمثل بداية النطاق القابل للتحرير.

```csharp
public EditableRangeStart EditableRangeStart { get; }
```

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

* class [EditableRangeStart](../../editablerangestart/)
* class [EditableRange](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
