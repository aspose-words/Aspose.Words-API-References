---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: DocumentPropertyCollection Item ملكية. إرجاع أDocumentProperty كائن باسم الخاصية في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

إرجاع أ[`DocumentProperty`](../../documentproperty/) كائن باسم الخاصية.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| معامل | وصف |
| --- | --- |
| name | اسم الخاصية غير حساس لحالة الأحرف المراد استرداده. |

## ملاحظات

عائدات`باطل` إذا لم يتم العثور على خاصية بالاسم المحدد.

## أمثلة

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على التاريخ والوقت.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

إرجاع أ[`DocumentProperty`](../../documentproperty/) كائن حسب الفهرس.

```csharp
public DocumentProperty this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | المؤشر الصفري[`DocumentProperty`](../../documentproperty/) لأسترجاع. |

## أمثلة

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
