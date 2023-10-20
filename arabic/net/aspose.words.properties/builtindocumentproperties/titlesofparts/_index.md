---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words لـ .NET
description: BuiltInDocumentProperties TitlesOfParts ملكية. تحدد كل سلسلة في المصفوفة اسم جزء في الوثيقة في C#.
type: docs
weight: 300
url: /ar/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

تحدد كل سلسلة في المصفوفة اسم جزء في الوثيقة.

```csharp
public string[] TitlesOfParts { get; set; }
```

## ملاحظات

لا يقوم Aspose.Words بتحديث هذه الخاصية.

## أمثلة

إظهار العلاقة بين خصائص "HeadingPairs" و"TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// يمكننا إيجاد القيم المجمعة لهذه المجموعات عبر
// "ملف" -> "الخصائص" -> "الخصائص المتقدمة" -> علامة التبويب "المحتويات".
// خاصية HeadingPairs عبارة عن مجموعة من <string, int> أزواج ذلك
// يحدد عدد أجزاء المستند التي يمتد عليها العنوان.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// تحتوي الخاصية TitlesOfParts على أسماء الأجزاء التي تنتمي إلى العناوين المذكورة أعلاه.
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

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
