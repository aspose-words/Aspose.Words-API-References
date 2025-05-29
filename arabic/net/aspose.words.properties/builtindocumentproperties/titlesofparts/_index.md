---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TitlesOfParts في BuiltInDocumentProperties. أدر أقسام المستند بسهولة باستخدام أسماء أجزاء واضحة وقابلة للتخصيص لتحسين التنظيم.
type: docs
weight: 330
url: /ar/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

يحدد كل سلسلة في المصفوفة اسم جزء في المستند.

```csharp
public string[] TitlesOfParts { get; set; }
```

## ملاحظات

لا يقوم Aspose.Words بتحديث هذه الخاصية.

## أمثلة

يُظهر العلاقة بين خصائص "HeadingPairs" و"TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// يمكننا العثور على القيم المجمعة لهذه المجموعات عبر
// "ملف" -> "خصائص" -> "خصائص متقدمة" -> علامة التبويب "المحتويات".
// خاصية HeadingPairs عبارة عن مجموعة من أزواج <string, int> التي
// يحدد عدد أجزاء المستند التي يمتد عبرها العنوان.
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

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
