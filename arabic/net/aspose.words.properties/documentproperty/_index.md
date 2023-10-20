---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Properties.DocumentProperty فصل. يمثل خاصية مستند مخصصة أو مضمنة في C#.
type: docs
weight: 4470
url: /ar/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

يمثل خاصية مستند مخصصة أو مضمنة.

لمعرفة المزيد، قم بزيارة[العمل مع خصائص الوثيقة](https://docs.aspose.com/words/net/work-with-document-properties/) مقالة توثيقية.

```csharp
public class DocumentProperty
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | يوضح ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | الحصول على مصدر خاصية المستند المخصص المرتبط. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | إرجاع اسم الخاصية. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | الحصول على نوع بيانات الخاصية. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | الحصول على قيمة الخاصية أو تحديدها. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | إرجاع قيمة الخاصية كقيمة منطقية. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | إرجاع قيمة الخاصية كمصفوفة بايت. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | إرجاع قيمة الخاصية كـ**التاريخ والوقت** بالتوقيت العالمي المنسق. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | إرجاع قيمة الخاصية مزدوجة. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | إرجاع قيمة الخاصية كعدد صحيح. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | تُرجع قيمة الخاصية كسلسلة منسقة وفقًا للغة المحلية الحالية. |

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

* class [DocumentPropertyCollection](../documentpropertycollection/)
* مساحة الاسم [Aspose.Words.Properties](../../aspose.words.properties/)
* المجسم [Aspose.Words](../../)
