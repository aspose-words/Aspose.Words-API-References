---
title: Document.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words لـ .NET
description: استكشف خاصية BuiltInDocumentProperties للوصول إلى خصائص المستند الأساسية، مما يعزز إدارة المستندات لديك وكفاءتها.
type: docs
weight: 50
url: /ar/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

يعيد مجموعة تمثل جميع خصائص المستند المضمنة.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

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

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
