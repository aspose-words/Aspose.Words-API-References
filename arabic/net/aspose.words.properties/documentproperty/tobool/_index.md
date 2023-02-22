---
title: DocumentProperty.ToBool
second_title: Aspose.Words لمراجع .NET API
description: DocumentProperty طريقة. إرجاع قيمة الخاصية على هيئة منطقية.
type: docs
weight: 60
url: /ar/net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

إرجاع قيمة الخاصية على هيئة منطقية.

```csharp
public bool ToBool()
```

### ملاحظات

يطرح استثناء إذا لم يكن نوع الخاصيةBoolean.

### أمثلة

يعرض طرق تحويل الأنواع المختلفة لخصائص المستند المخصصة.

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


