---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words для .NET
description: Изучите свойство HeadingPairs в BuiltInDocumentProperties, чтобы легко управлять заголовками документов и улучшить их организацию.
type: docs
weight: 110
url: /ru/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Указывает заголовки документов и их названия.

```csharp
public object[] HeadingPairs { get; set; }
```

## Примечания

Каждая пара заголовков занимает два элемента в этом массиве.

Первый элемент пары — этоString и указывает имя заголовка. Второй элемент пары — этоInt32 и указывает количество частей document для этого заголовка в[`TitlesOfParts`](../titlesofparts/) свойство.

Общая сумма подсчетов для всех пар заголовков в этом свойстве должна быть равна количеству элементов в x000d[`TitlesOfParts`](../titlesofparts/) свойство.

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
