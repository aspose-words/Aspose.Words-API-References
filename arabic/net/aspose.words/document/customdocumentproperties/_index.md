---
title: Document.CustomDocumentProperties
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. إرجاع مجموعة تمثل كافة خصائص المستند المخصصة للمستند.
type: docs
weight: 70
url: /ar/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

إرجاع مجموعة تمثل كافة خصائص المستند المخصصة للمستند.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

### أمثلة

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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


