---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى كائنات DocumentProperty بسهولة باستخدام عنصر DocumentPropertyCollection. استرجع الخصائص بالاسم لإدارة مستندات سلسة.
type: docs
weight: 20
url: /ar/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

يعيد[`DocumentProperty`](../../documentproperty/) الكائن حسب اسم الخاصية.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| معامل | وصف |
| --- | --- |
| name | الاسم غير الحساس لحالة الأحرف للخاصية التي سيتم استردادها. |

## ملاحظات

الإرجاعات`باطل` إذا لم يتم العثور على خاصية بالاسم المحدد.

## أمثلة

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على تاريخ ووقت.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

يعيد[`DocumentProperty`](../../documentproperty/) الكائن حسب index.

```csharp
public DocumentProperty this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | مؤشر قائم على الصفر[`DocumentProperty`](../../documentproperty/) لاسترجاع. |

## أمثلة

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
