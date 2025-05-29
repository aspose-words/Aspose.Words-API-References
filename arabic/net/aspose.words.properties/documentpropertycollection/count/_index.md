---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Count في DocumentPropertyCollection لاسترداد عدد العناصر في مجموعتك بسهولة لإدارة البيانات بكفاءة.
type: docs
weight: 10
url: /ar/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

يحصل على عدد العناصر في المجموعة.

```csharp
public int Count { get; }
```

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

* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
