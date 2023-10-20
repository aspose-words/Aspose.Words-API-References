---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words لـ .NET
description: BuiltInDocumentProperties HeadingPairs ملكية. تحديد عناوين المستندات وأسمائها في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

تحديد عناوين المستندات وأسمائها.

```csharp
public object[] HeadingPairs { get; set; }
```

## ملاحظات

يحتل كل زوج عنوان عنصرين في هذه المصفوفة.

العنصر الأول في الزوج هو أString ويحدد اسم العنوان. العنصر الثاني من الزوج هوInt32 ويحدد عدد أجزاء document لهذا العنوان في ملف[`TitlesOfParts`](../titlesofparts/) ملكية.

يجب أن يكون إجمالي عدد الأعداد لجميع أزواج العناوين في هذه الخاصية مساويًا لعدد من العناصر في[`TitlesOfParts`](../titlesofparts/) ملكية.

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
