---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words لـ .NET
description: استكشف خاصية HeadingPairs في BuiltInDocumentProperties لإدارة عناوين المستندات بسهولة وتحسين تنظيم المستندات لديك.
type: docs
weight: 110
url: /ar/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

يحدد عناوين المستندات وأسمائها.

```csharp
public object[] HeadingPairs { get; set; }
```

## ملاحظات

يشغل كل زوج من العناوين عنصرين في هذه المصفوفة.

العنصر الأول من الزوج هوString ويحدد اسم العنوان. العنصر الثاني من الزوج هوInt32 ويحدد عدد أجزاء document لهذا العنوان في[`TitlesOfParts`](../titlesofparts/) ملكية.

يجب أن يكون المجموع الإجمالي لعدد كل أزواج العناوين في هذه الخاصية مساويًا لعدد العناصر في [`TitlesOfParts`](../titlesofparts/) ملكية.

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
