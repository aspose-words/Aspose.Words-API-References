---
title: OdsoFieldMapData.Column
linktitle: Column
articleTitle: Column
second_title: Aspose.Words для .NET
description: OdsoFieldMapData Column свойство. Указывает отсчитываемый от нуля индекс столбца во внешнем источнике данных который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. Значение по умолчанию  0 на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.settings/odsofieldmapdata/column/
---
## OdsoFieldMapData.Column property

Указывает отсчитываемый от нуля индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. Значение по умолчанию — 0.

```csharp
public int Column { get; set; }
```

## Примеры

Показывает, как получить доступ к коллекции данных, которая сопоставляет столбцы источника данных с полями слияния.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// Эта коллекция определяет, как слияние почты будет сопоставлять столбцы из источника данных
// к предопределенным полям MERGEFIELD, ADDRESSBLOCK и GREETINGLINE.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// Клонируем элементы этой коллекции.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Используйте элементы метода «RemoveAt» индивидуально по индексу.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Используйте метод «Очистить», чтобы очистить всю коллекцию сразу.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Смотрите также

* class [OdsoFieldMapData](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
