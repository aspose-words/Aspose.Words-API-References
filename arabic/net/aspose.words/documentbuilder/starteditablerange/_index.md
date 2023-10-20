---
title: DocumentBuilder.StartEditableRange
linktitle: StartEditableRange
articleTitle: StartEditableRange
second_title: Aspose.Words لـ .NET
description: DocumentBuilder StartEditableRange طريقة. يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير في C#.
type: docs
weight: 630
url: /ar/net/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder.StartEditableRange method

يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير.

```csharp
public EditableRangeStart StartEditableRange()
```

### قيمة الإرجاع

عقدة بداية النطاق القابل للتحرير التي تم إنشاؤها للتو.

## ملاحظات

يمكن أن يتداخل النطاق القابل للتحرير في المستند ويمتد إلى أي نطاق. لإنشاء نطاق صالح قابل للتحرير، يلزمك الاتصال بكليهما`StartEditableRange` و[`EndEditableRange`](../endeditablerange/) أو[`EndEditableRange`](../endeditablerange/) طُرق.

سيتم تجاهل النطاق القابل للتحرير الذي تم تكوينه بشكل سيئ عند حفظ المستند.

## أمثلة

يوضح كيفية إنشاء نطاقات متداخلة قابلة للتحرير.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// أنشئ نطاقين متداخلين قابلين للتحرير.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// حاليًا، يوجد مؤشر إدراج عقدة منشئ المستندات في أكثر من نطاق قابل للتحرير المستمر.
// عندما نريد إنهاء نطاق قابل للتحرير في هذه الحالة،
// نحتاج إلى تحديد النطاق الذي نرغب في إنهائه بتمرير عقدة EditableRangeStart الخاصة به.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// إذا كانت منطقة النص تحتوي على نطاقين متداخلين قابلين للتحرير مع مجموعات محددة،
// يتم منع المجموعة المدمجة من المستخدمين المستبعدين من كلا المجموعتين من تحريرها.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

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

* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
