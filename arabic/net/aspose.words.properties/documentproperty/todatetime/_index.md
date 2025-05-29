---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words لـ .NET
description: حوّل DocumentProperty إلى تاريخ ووقت UTC بسهولة. احصل على تواريخ زمنية دقيقة وحسّن إدارة بياناتك بأسلوبنا الموثوق.
type: docs
weight: 80
url: /ar/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

يعيد قيمة الخاصية كـ**التاريخ والوقت** بالتوقيت العالمي المنسق.

```csharp
public DateTime ToDateTime()
```

## ملاحظات

يُلقي استثناءً إذا لم يكن نوع الخاصيةDateTime.

يقوم Microsoft Word بتخزين جزء التاريخ فقط (بدون وقت) لخصائص التاريخ المخصصة.

## أمثلة

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على تاريخ ووقت.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
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
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
