---
title: EditableRangeEnd.EditableRangeStart
second_title: Aspose.Words لمراجع .NET API
description: EditableRangeEnd ملكية. EditableRangeStart المقابل  تم استلامه بواسطة ID.
type: docs
weight: 10
url: /ar/net/aspose.words/editablerangeend/editablerangestart/
---
## EditableRangeEnd.EditableRangeStart property

EditableRangeStart المقابل ، تم استلامه بواسطة ID.

```csharp
public EditableRangeStart EditableRangeStart { get; }
```

### أمثلة

يوضح كيفية العمل بنطاق قابل للتحرير.

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

// يحتوي النطاق القابل للتعديل جيدًا على عقدة البداية ونقطة النهاية.
// هذه العقد لها معرّفات متطابقة وتشمل عقدًا قابلة للتحرير.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// ترتبط أجزاء مختلفة من النطاق القابل للتعديل ببعضها البعض.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// يمكننا الوصول إلى أنواع العقدة لكل جزء مثل هذا. النطاق القابل للتحرير في حد ذاته ليس عقدة ،
// ولكن كيان يتكون من بداية ونهاية ومحتوياتها المرفقة.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// إزالة نطاق قابل للتحرير. ستبقى جميع العقد التي كانت داخل النطاق سليمة.
editableRange.Remove();
```

### أنظر أيضا

* class [EditableRangeStart](../../editablerangestart/)
* class [EditableRangeEnd](../)
* مساحة الاسم [Aspose.Words](../../editablerangeend/)
* المجسم [Aspose.Words](../../../)


