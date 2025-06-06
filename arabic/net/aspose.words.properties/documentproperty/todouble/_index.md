---
title: DocumentProperty.ToDouble
linktitle: ToDouble
articleTitle: ToDouble
second_title: Aspose.Words لـ .NET
description: حوّل قيم DocumentProperty إلى قيم مضاعفة بسهولة باستخدام طريقة ToDouble. تمتع بمعالجة دقيقة للبيانات في تطبيقاتك اليوم!
type: docs
weight: 90
url: /ar/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

يعيد قيمة الخاصية على هيئة double.

```csharp
public double ToDouble()
```

## ملاحظات

يطرح استثناءً إذا لم يكن نوع الخاصيةNumber .

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
