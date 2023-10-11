---
title: DocumentProperty.ToDateTime
second_title: Aspose.Words لمراجع .NET API
description: DocumentProperty طريقة. إرجاع قيمة الخاصية كـ التاريخ والوقت بالتوقيت العالمي المنسق.
type: docs
weight: 80
url: /ar/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

إرجاع قيمة الخاصية كـ **التاريخ والوقت** بالتوقيت العالمي المنسق.

```csharp
public DateTime ToDateTime()
```

### ملاحظات

يطرح استثناءً إذا لم يكن نوع الخاصية كذلكDateTime.

يقوم Microsoft Word بتخزين جزء التاريخ فقط (بدون وقت) لخصائص التاريخ المخصصة.

### أمثلة

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على التاريخ والوقت.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

يعرض طرق تحويل النوع المختلفة لخصائص المستند المخصصة.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### أنظر أيضا

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../documentproperty/)
* المجسم [Aspose.Words](../../../)


