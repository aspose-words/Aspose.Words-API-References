---
title: DocumentProperty.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentProperty ToString، التي تقوم بتنسيق قيم الخصائص كسلاسل استنادًا إلى الإعدادات المحلية، مما يعزز عرض البيانات وتجربة المستخدم.
type: docs
weight: 110
url: /ar/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

يعيد قيمة الخاصية كسلسلة منسقة وفقًا للإعدادات المحلية الحالية.

```csharp
public override string ToString()
```

## ملاحظات

تحويل خاصية منطقية إلى "Y" أو "N". تحويل خاصية تاريخ إلى سلسلة تاريخ قصيرة. بالنسبة لجميع الأنواع الأخرى، تحويل خاصية باستخدام Object.ToString().

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

يوضح كيفية العمل مع خصائص المستند المخصصة.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// تحتوي كل مستند على مجموعة من الخصائص المخصصة، والتي، مثل الخصائص المضمنة، عبارة عن أزواج من القيمة الأساسية.
 // تحتوي الوثيقة على قائمة ثابتة من الخصائص المضمنة. يُنشئ المستخدم جميع الخصائص المخصصة.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### أنظر أيضا

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
