---
title: EditableRangeStart.EditableRange
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words لـ .NET
description: EditableRangeStart EditableRange ملكية. يحصل على كائن الواجهة الذي يغلف هذا النطاق القابل للتحرير بداية ونهاية في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/editablerangestart/editablerange/
---
## EditableRangeStart.EditableRange property

يحصل على كائن الواجهة الذي يغلف هذا النطاق القابل للتحرير بداية ونهاية.

```csharp
public EditableRange EditableRange { get; }
```

## أمثلة

يوضح كيفية العمل مع نطاق قابل للتحرير.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// النطاقات القابلة للتحرير تسمح لنا بترك أجزاء من المستندات المحمية مفتوحة للتحرير.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// يحتوي النطاق القابل للتحرير المصمم جيدًا على عقدة بداية وعقدة نهاية.
// تحتوي هذه العقد على معرفات متطابقة وتشمل عقدًا قابلة للتحرير.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// ترتبط الأجزاء المختلفة من النطاق القابل للتحرير ببعضها البعض.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// يمكننا الوصول إلى أنواع العقد لكل جزء بهذه الطريقة. النطاق القابل للتحرير في حد ذاته ليس عقدة،
// ولكن كيان يتكون من البداية والنهاية ومحتوياتها المغلقة.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// إزالة نطاق قابل للتحرير. جميع العقد التي كانت داخل النطاق ستبقى سليمة.
editableRange.Remove();
```

### أنظر أيضا

* class [EditableRange](../../editablerange/)
* class [EditableRangeStart](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
