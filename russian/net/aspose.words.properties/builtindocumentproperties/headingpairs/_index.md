---
title: BuiltInDocumentProperties.HeadingPairs
second_title: Справочник по API Aspose.Words для .NET
description: BuiltInDocumentProperties свойство. Указывает заголовки документов и их имена.
type: docs
weight: 110
url: /ru/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Указывает заголовки документов и их имена.

```csharp
public object[] HeadingPairs { get; set; }
```

### Примечания

Каждая пара заголовков занимает два элемента в этом массиве.

Первый элемент пары — этоString и указывает имя заголовка. Второй элемент пары — этоInt32 и указывает количество частей document для этого заголовка в[`TitlesOfParts`](../titlesofparts/) свойство.

Общая сумма счетчиков для всех пар заголовков в этом свойстве должна быть равна количеству элементов в[`TitlesOfParts`](../titlesofparts/) свойство.

Aspose.Words не обновляет это свойство.

### Примеры

Показывает связь между свойствами "HeadingPairs" и "TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Мы можем найти объединенные значения этих коллекций через
// "Файл" -> «Свойства» -> «Дополнительные свойства» -> Вкладка «Содержание».
// Свойство HeadingPairs представляет собой коллекцию <string, int> пары, которые
// определяет, сколько частей документа охватывает заголовок.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Свойство TitlesOfParts содержит названия частей, принадлежащих к указанным выше заголовкам.
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


