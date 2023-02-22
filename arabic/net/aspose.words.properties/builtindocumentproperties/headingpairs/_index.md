---
title: BuiltInDocumentProperties.HeadingPairs
second_title: Aspose.Words لمراجع .NET API
description: BuiltInDocumentProperties ملكية. تحديد عناوين المستند وأسمائها .
type: docs
weight: 110
url: /ar/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

تحديد عناوين المستند وأسمائها .

```csharp
public object[] HeadingPairs { get; set; }
```

### ملاحظات

يحتل كل زوج عنوان عنصرين في هذه المجموعة.

العنصر الأول في الزوج هوString ويحدد اسم العنوان . العنصر الثاني للزوج هوInt32 ويحدد عدد أجزاء document لهذا العنوان في ملف[`TitlesOfParts`](../titlesofparts/) منشأه.

يجب أن يكون إجمالي عدد الأعداد لكل أزواج العناوين في هذه الخاصية مساويًا لـ عدد العناصر في[`TitlesOfParts`](../titlesofparts/) منشأه.

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

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../builtindocumentproperties/)
* المجسم [Aspose.Words](../../../)


