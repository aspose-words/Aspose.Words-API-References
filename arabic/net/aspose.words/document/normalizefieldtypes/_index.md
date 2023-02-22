---
title: Document.NormalizeFieldTypes
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. يغير قيم نوع الحقلFieldType منFieldStart وFieldSeparator وFieldEnd في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في أكواد الحقول.
type: docs
weight: 610
url: /ar/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

يغير قيم نوع الحقل[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) من[`FieldStart`](../../../aspose.words.fields/fieldstart/) و[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) و[`FieldEnd`](../../../aspose.words.fields/fieldend/) في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في أكواد الحقول.

```csharp
public void NormalizeFieldTypes()
```

### ملاحظات

استخدم هذه الطريقة بعد تغييرات المستند التي تؤثر على أنواع الحقول.

لتغيير قيم نوع الحقل في جزء معين من المستند استخدم[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### أمثلة

يوضح كيفية الحفاظ على تحديث نوع الحقل برمز الحقل الخاص به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words يكتشف تلقائيًا أنواع الحقول بناءً على أكواد الحقول.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// قم بتغيير النص الأولي للحقل يدويًا ، والذي يحدد رمز الحقل.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];

// لقد أدى تغيير رمز الحقل إلى تغيير هذا الحقل إلى نوع مختلف ،
// ولكن لا تزال خصائص نوع الحقل تعرض النوع القديم.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// تحديث تلك الخصائص بهذه الطريقة لعرض القيمة الحالية.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType); 
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


