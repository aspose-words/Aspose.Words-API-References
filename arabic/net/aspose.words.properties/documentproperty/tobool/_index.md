---
title: DocumentProperty.ToBool
linktitle: ToBool
articleTitle: ToBool
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentProperty ToBool التي تقوم بتحويل قيم الخصائص إلى قيم منطقية بكفاءة من أجل التعامل السلس مع البيانات وتحسين كفاءة الترميز.
type: docs
weight: 60
url: /ar/net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

يعيد قيمة الخاصية كقيمة منطقية.

```csharp
public bool ToBool()
```

## ملاحظات

يُلقي استثناءً إذا لم يكن نوع الخاصيةBoolean.

## أمثلة

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
