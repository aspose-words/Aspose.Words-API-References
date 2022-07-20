---
title: TitlesOfParts
second_title: Aspose.Words لمراجع .NET API
description: تحدد كل سلسلة في المصفوفة اسم جزء في المستند.
type: docs
weight: 300
url: /ar/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

تحدد كل سلسلة في المصفوفة اسم جزء في المستند.

```csharp
public string[] TitlesOfParts { get; set; }
```

### ملاحظات

Aspose.Words لا تقوم بتحديث هذه الخاصية.

### أمثلة

يظهر العلاقة بين خصائص "HeadingPairs" و "TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// يمكننا العثور على القيم المجمعة لهذه المجموعات عبر
// "ملف" - >. "خصائص" - >. "خصائص متقدمة" - >. علامة التبويب "المحتويات".
// الخاصية HeadingPairs هي مجموعة من < string، int > أزواج ذلك
// يحدد عدد أجزاء المستند التي يمتد العنوان عبرها.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// تحتوي الخاصية TitlesOfParts على أسماء الأجزاء التي تنتمي إلى العناوين أعلاه.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../../builtindocumentproperties)
* مساحة الاسم [Aspose.Words.Properties](../../builtindocumentproperties)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->