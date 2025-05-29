---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.OdsoFieldMappingType для эффективного сопоставления полей слияния с внешними источниками данных. Улучшите автоматизацию документов сегодня!
type: docs
weight: 6750
url: /ru/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

Указывает возможные типы, используемые для указания того, сопоставлено ли заданное поле слияния со столбцом в заданном внешнем источнике данных.

```csharp
public enum OdsoFieldMappingType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Column | `0` | Указывает, что поле слияния почты сопоставлено со столбцом в указанном внешнем источнике данных. |
| Null | `1` | Указывает, что поле слияния почты не сопоставлено со столбцом в указанном внешнем источнике данных. |
| Default | `1` | РавноNull . |

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

// Используем метод «RemoveAt» для отдельных элементов по индексу.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// Используйте метод «Очистить», чтобы очистить всю коллекцию сразу.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Смотрите также

* property [Type](../odsofieldmapdata/type/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
