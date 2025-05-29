---
title: Document.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words لـ .NET
description: قم بتحسين مستندك باستخدام طريقة NormalizeFieldTypes، مما يضمن توافق جميع قيم نوع الحقل مع رموز الحقل لتحسين التناسق والدقة.
type: docs
weight: 670
url: /ar/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

تغيير قيم نوع الحقل[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../../aspose.words.fields/fieldstart/) ،[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ،[`FieldEnd`](../../../aspose.words.fields/fieldend/) في المستند بأكمله بحيث تتوافق مع أنواع الحقول الموجودة في رموز الحقول.

```csharp
public void NormalizeFieldTypes()
```

## ملاحظات

استخدم هذه الطريقة بعد إجراء تغييرات على المستند تؤثر على أنواع الحقول.

لتغيير قيم نوع الحقل في جزء معين من المستند، استخدم[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

## أمثلة

يوضح كيفية الحفاظ على تحديث نوع الحقل باستخدام رمز الحقل الخاص به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// يكتشف Aspose.Words أنواع الحقول تلقائيًا استنادًا إلى رموز الحقول.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// تغيير النص الخام للحقل يدويًا، والذي يحدد رمز الحقل.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// أدى تغيير رمز الحقل إلى تغيير هذا الحقل إلى حقل من نوع مختلف،
// ولكن خصائص نوع الحقل لا تزال تعرض النوع القديم.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// قم بتحديث تلك الخصائص باستخدام هذه الطريقة لعرض القيمة الحالية.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
