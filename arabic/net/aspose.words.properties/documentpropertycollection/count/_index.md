---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: DocumentPropertyCollection Count ملكية. الحصول على عدد العناصر الموجودة في المجموعة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

الحصول على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

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

* class [DocumentPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
