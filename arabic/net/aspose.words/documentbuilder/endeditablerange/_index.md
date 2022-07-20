---
title: EndEditableRange
second_title: Aspose.Words لمراجع .NET API
description: وضع علامة على الموضع الحالي في المستند كنهاية نطاق قابل للتحرير.
type: docs
weight: 210
url: /ar/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

وضع علامة على الموضع الحالي في المستند كنهاية نطاق قابل للتحرير.

```csharp
public EditableRangeEnd EndEditableRange()
```

### قيمة الإرجاع

عقدة نهاية النطاق القابلة للتحرير التي تم إنشاؤها للتو.

### ملاحظات

يمكن أن يتداخل النطاق القابل للتحرير في المستند ويمتد إلى أي نطاق. لإنشاء نطاق صالح قابل للتحرير ، تحتاج إلى الاتصال بكليهما[`StartEditableRange`](../starteditablerange) و`EndEditableRange` أو[`EndEditableRange`](../endeditablerange)طُرق.

سيتم تجاهل النطاق القابل للتحرير الذي تم تكوينه بشكل سيئ عند حفظ المستند.

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

* class [EditableRangeEnd](../../editablerangeend)
* class [DocumentBuilder](../../documentbuilder)
* مساحة الاسم [Aspose.Words](../../documentbuilder)
* المجسم [Aspose.Words](../../../)

---

## EndEditableRange(EditableRangeStart) {#endeditablerange_1}

وضع علامة على الموضع الحالي في المستند كنهاية نطاق قابل للتحرير.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| start | EditableRangeStart | يبدأ هذا النطاق القابل للتحرير. |

### قيمة الإرجاع

عقدة نهاية النطاق القابلة للتحرير التي تم إنشاؤها للتو.

### ملاحظات

استخدم هذا التحميل الزائد أثناء إنشاء نطاقات متداخلة قابلة للتحرير.

يمكن أن يتداخل النطاق القابل للتحرير في المستند ويمتد إلى أي نطاق. لإنشاء نطاق صالح قابل للتحرير ، تحتاج إلى الاتصال بكليهما[`StartEditableRange`](../starteditablerange) و[`EndEditableRange`](../endeditablerange) أو`EndEditableRange`طُرق.

سيتم تجاهل النطاق القابل للتحرير الذي تم تكوينه بشكل سيئ عند حفظ المستند.

### أمثلة

يوضح كيفية إنشاء نطاقات متداخلة قابلة للتحرير.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// إنشاء نطاقين متداخلين قابلين للتحرير.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// حاليًا ، يوجد مؤشر إدراج عقدة منشئ المستندات في أكثر من نطاق قابل للتحرير مستمر.
// عندما نريد إنهاء نطاق قابل للتعديل في هذه الحالة ،
// نحتاج إلى تحديد النطاقات التي نرغب في إنهاؤها بتمرير عقدة EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// إذا كانت منطقة النص تشتمل على نطاقين قابلين للتعديل متداخلين مع مجموعات محددة ،
// تم منع المجموعة المدمجة من المستخدمين المستبعدة من قبل المجموعتين من تحريرها.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### أنظر أيضا

* class [EditableRangeEnd](../../editablerangeend)
* class [EditableRangeStart](../../editablerangestart)
* class [DocumentBuilder](../../documentbuilder)
* مساحة الاسم [Aspose.Words](../../documentbuilder)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
