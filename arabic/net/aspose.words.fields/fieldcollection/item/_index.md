---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldCollection Item، وقم بالوصول بسهولة إلى الحقول عن طريق الفهرس وعزز إدارة بياناتك بسهولة ودقة.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

يعيد حقلًا عند الفهرس المحدد.

```csharp
public Field this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للمجموعة. |

## ملاحظات

المؤشر يعتمد على الصفر.

يُسمح بالمؤشرات السلبية وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فسوف يؤدي هذا إلى إرجاع مرجع فارغ.

إذا كان الفهرس سلبيًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فسيؤدي هذا إلى إرجاع مرجع فارغ.

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
// 1 - الحصول على حقل لإزالة نفسه:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - الحصول على المجموعة لإزالة الحقل الذي نمرره إلى طريقة الإزالة الخاصة به:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - إزالة حقل من مجموعة عند الفهرس:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - إزالة جميع الحقول من المجموعة مرة واحدة:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### أنظر أيضا

* class [Field](../../field/)
* class [FieldCollection](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
