---
title: Document.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words لـ .NET
description: استكشف خاصية CustomDocumentProperties للوصول إلى كافة خصائص المستند المخصصة وإدارتها بكفاءة، مما يؤدي إلى تحسين وظائف المستند لديك.
type: docs
weight: 80
url: /ar/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

يعيد مجموعة تمثل جميع خصائص المستند المخصصة للمستند.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
