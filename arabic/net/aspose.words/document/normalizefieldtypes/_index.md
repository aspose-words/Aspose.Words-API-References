---
title: Document.NormalizeFieldTypes
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. تغيير قيم نوع الحقلFieldType لFieldStart FieldSeparator FieldEnd في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في رموز الحقول.
type: docs
weight: 650
url: /ar/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

تغيير قيم نوع الحقل[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في رموز الحقول.

```csharp
public void NormalizeFieldTypes()
```

### ملاحظات

استخدم هذه الطريقة بعد تغييرات المستند التي تؤثر على أنواع الحقول.

لتغيير قيم نوع الحقل في جزء معين من استخدام المستند[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### أمثلة

يوضح كيفية تحديث نوع الحقل باستخدام رمز الحقل الخاص به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words يكتشف تلقائيًا أنواع الحقول بناءً على رموز الحقول.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// قم بتغيير النص الأولي للحقل يدويًا، والذي يحدد رمز الحقل.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// تغيير رمز الحقل أدى إلى تغيير هذا الحقل إلى نوع مختلف،
// لكن خصائص نوع الحقل لا تزال تعرض النوع القديم.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// قم بتحديث هذه الخصائص بهذه الطريقة لعرض القيمة الحالية.
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


