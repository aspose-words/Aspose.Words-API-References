---
title: DocumentProperty.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة قيم DocumentProperty بكفاءة - استرداد قيم الخصائص أو تحديثها بسهولة لتحسين التحكم في المستندات والإنتاجية.
type: docs
weight: 50
url: /ar/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

يحصل على قيمة الخاصية أو يعينها.

```csharp
public object Value { get; set; }
```

## ملاحظات

لا يمكن أن يكون`باطل`.

## أمثلة

يوضح كيفية العمل مع خصائص المستند المضمنة.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

//يحتوي كائن "المستند" على بعض بياناته الوصفية في أعضائه.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// تقوم الوثيقة أيضًا بتخزين البيانات الوصفية في خصائصها المضمنة.
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
