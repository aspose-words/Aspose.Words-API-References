---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.OdsoFieldMapData для бесшовного сопоставления внешних столбцов данных с предопределенными полями слияния документов, что повышает автоматизацию документов.
type: docs
weight: 6730
url: /ru/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределенными полями слияния в документе.

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public class OdsoFieldMapData
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Указывает индекс столбца во внешнем источнике данных, начинающийся с нуля, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. Значение по умолчанию — 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Указывает предопределенное имя поля слияния, которое должно быть сопоставлено с номером столбца , указанным[`Column`](./column/) свойство в этом отображении поля. Значение по умолчанию — пустая строка. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан[`Column`](./column/)свойство. Значение по умолчанию — пустая строка. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Указывает, сопоставлено ли заданное поле слияния со столбцом в заданном внешнем источнике данных. Значение по умолчанию:Default . |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Возвращает глубокий клон этого объекта. |

## Примечания

Microsoft Word предоставляет некоторые предопределенные имена полей слияния, которые он позволяет вставлять в документ как MERGEFIELD или , использовать в полях ADDRESSBLOCK или GREETINGLINE. Информация, указанная в`OdsoFieldMapData` позволяет сопоставить один столбец во внешнем источнике данных с одним предопределенным полем слияния.

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

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
