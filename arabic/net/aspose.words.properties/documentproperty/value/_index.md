---
title: DocumentProperty.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words لـ .NET
description: DocumentProperty Value ملكية. الحصول على قيمة الخاصية أو تحديدها في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

الحصول على قيمة الخاصية أو تحديدها.

```csharp
public object Value { get; set; }
```

## ملاحظات

لا يمكن`باطل`.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المضمنة.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// يحتوي كائن "المستند" على بعض بيانات التعريف الخاصة به في أعضائه.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// يقوم المستند أيضًا بتخزين البيانات التعريفية في خصائصه المضمنة.
// كل خاصية مضمنة هي عضو في كائن "BuiltInDocumentProperties" الخاص بالمستند.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // قد تقوم بعض الخصائص بتخزين قيم متعددة.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### أنظر أيضا

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
