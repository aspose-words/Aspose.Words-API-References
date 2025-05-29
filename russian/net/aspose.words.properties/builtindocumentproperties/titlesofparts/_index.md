---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TitlesOfParts в BuiltInDocumentProperties. Легко управляйте разделами документа с помощью понятных, настраиваемых имен частей для улучшенной организации.
type: docs
weight: 330
url: /ru/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Каждая строка в массиве определяет имя части в документе.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Примечания

Aspose.Words не обновляет это свойство.

## Примеры

Показывает связь между свойствами «HeadingPairs» и «TitlesOfParts».

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Мы можем найти объединенные значения этих коллекций через
// «Файл» -> «Свойства» -> «Дополнительные свойства» -> вкладка «Содержимое».
// Свойство HeadingPairs — это коллекция пар <string, int>, которые
// определяет, сколько частей документа охватывает заголовок.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Свойство TitlesOfParts содержит названия частей, которые относятся к вышеуказанным заголовкам.
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
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
