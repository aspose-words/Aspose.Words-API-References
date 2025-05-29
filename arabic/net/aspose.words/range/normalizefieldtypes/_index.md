---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words لـ .NET
description: حوّل أنواع الحقول باستخدام طريقة NormalizeFieldTypes. تأكد من محاذاة FieldStart وFieldSeparator وFieldEnd مع رموز الحقول المحددة لضمان معالجة سلسة للبيانات.
type: docs
weight: 90
url: /ar/net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

تغيير قيم نوع الحقل[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) ل[`FieldStart`](../../../aspose.words.fields/fieldstart/) ،[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ،[`FieldEnd`](../../../aspose.words.fields/fieldend/) في هذا النطاق بحيث تتوافق مع أنواع الحقول الموجودة في أكواد الحقول.

```csharp
public void NormalizeFieldTypes()
```

## ملاحظات

استخدم هذه الطريقة بعد إجراء تغييرات على المستند تؤثر على أنواع الحقول.

لتغيير قيم نوع الحقل في المستند بأكمله، استخدم[`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

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

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
