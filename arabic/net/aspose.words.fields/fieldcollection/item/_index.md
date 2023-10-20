---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: FieldCollection Item ملكية. إرجاع حقل في الفهرس المحدد في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

إرجاع حقل في الفهرس المحدد.

```csharp
public Field this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس في المجموعة. |

## ملاحظات

المؤشر قائم على الصفر.

الفهارس السالبة مسموح بها وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر الموجودة في القائمة، فسيُرجع هذا مرجعًا فارغًا.

إذا كان الفهرس سالبًا وقيمته المطلقة أكبر من عدد العناصر الموجودة في القائمة، فسيُرجع هذا مرجعًا فارغًا.

## أمثلة

يوضح كيفية إزالة الحقول من مجموعة الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// فيما يلي أربع طرق لإزالة الحقول من مجموعة الحقول.
// 1 - احصل على حقل لإزالة نفسه:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - احصل على المجموعة لإزالة الحقل الذي نمرره إلى طريقة الإزالة الخاصة به:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - إزالة حقل من مجموعة في فهرس:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - قم بإزالة كافة الحقول من المجموعة مرة واحدة:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### أنظر أيضا

* class [Field](../../field/)
* class [FieldCollection](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
