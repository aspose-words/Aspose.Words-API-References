---
title: FieldCollection.Remove
second_title: Aspose.Words لمراجع .NET API
description: FieldCollection طريقة. إزالة الحقل المحدد من هذه المجموعة ومن المستند.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection.Remove method

إزالة الحقل المحدد من هذه المجموعة ومن المستند.

```csharp
public void Remove(Field field)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| field | Field | حقل لإزالة. |

### أمثلة

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
* مساحة الاسم [Aspose.Words.Fields](../../fieldcollection/)
* المجسم [Aspose.Words](../../../)


