---
title: BuiltInDocumentProperties.TitlesOfParts
second_title: Справочник по API Aspose.Words для .NET
description: BuiltInDocumentProperties свойство. Каждая строка в массиве указывает имя части в документе.
type: docs
weight: 300
url: /ru/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Каждая строка в массиве указывает имя части в документе.

```csharp
public string[] TitlesOfParts { get; set; }
```

### Примечания

Aspose.Words не обновляет это свойство.

### Примеры

Показывает взаимосвязь между свойствами "HeadingPairs" и "TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Мы можем найти объединенные значения этих коллекций через
// "Файл" -> "Свойства" -> "Дополнительные свойства" -> Вкладка «Содержание».
// Свойство HeadingPairs представляет собой набор <string, int> пары, которые
// определяет, сколько частей документа охватывает заголовок.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Свойство TitlesOfParts содержит имена частей, принадлежащих вышеуказанным заголовкам.
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

### Смотрите также

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../builtindocumentproperties/)
* сборка [Aspose.Words](../../../)


