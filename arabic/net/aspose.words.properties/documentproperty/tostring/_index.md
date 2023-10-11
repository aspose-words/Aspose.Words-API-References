---
title: DocumentProperty.ToString
second_title: Aspose.Words لمراجع .NET API
description: DocumentProperty طريقة. تُرجع قيمة الخاصية كسلسلة منسقة وفقًا للغة المحلية الحالية.
type: docs
weight: 110
url: /ar/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

تُرجع قيمة الخاصية كسلسلة منسقة وفقًا للغة المحلية الحالية.

```csharp
public override string ToString()
```

### ملاحظات

تحويل خاصية منطقية إلى "Y" أو "N". تحويل خاصية تاريخ إلى سلسلة تاريخ قصيرة. بالنسبة لجميع الأنواع الأخرى، يتم تحويل خاصية باستخدام Object.ToString().

### أمثلة

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

// يحتوي كل مستند على مجموعة من الخصائص المخصصة، والتي، مثل الخصائص المضمنة، هي أزواج قيمة المفتاح.
 // يحتوي المستند على قائمة ثابتة بالخصائص المضمنة. يقوم المستخدم بإنشاء كافة الخصائص المخصصة.
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
* مساحة الاسم [Aspose.Words.Properties](../../documentproperty/)
* المجسم [Aspose.Words](../../../)


