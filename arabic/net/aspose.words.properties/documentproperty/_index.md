---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Properties.DocumentProperty لإدارة خصائص المستندات المخصصة والمضمنة بكفاءة. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 5200
url: /ar/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

يمثل خاصية مستند مخصصة أو مضمنة.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص المستند](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public class DocumentProperty
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | يُظهر ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | يحصل على مصدر خاصية مستند مخصص مرتبط. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | يعيد اسم الخاصية. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | يحصل على نوع بيانات الخاصية. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | يحصل على قيمة الخاصية أو يعينها. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | يعيد قيمة الخاصية كقيمة منطقية. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | يعيد قيمة الخاصية كمصفوفة بايت. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | يعيد قيمة الخاصية كـ**التاريخ والوقت** بالتوقيت العالمي المنسق. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | يعيد قيمة الخاصية على هيئة double. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | يعيد قيمة الخاصية كعدد صحيح. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | يعيد قيمة الخاصية كسلسلة منسقة وفقًا للإعدادات المحلية الحالية. |

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

* class [DocumentPropertyCollection](../documentpropertycollection/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)
