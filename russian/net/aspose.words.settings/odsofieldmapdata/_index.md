---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words для .NET
description: Aspose.Words.Settings.OdsoFieldMapData сорт. Указывает как столбец во внешнем источнике данных должен быть сопоставлен с предопределенными полями слияния в документе на С#.
type: docs
weight: 5900
url: /ru/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределенными полями слияния в документе.

Чтобы узнать больше, посетите[Слияние почты и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) статья документации.

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
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | Указывает отсчитываемый от нуля индекс столбца во внешнем источнике данных, который должен быть сопоставлен с локальным именем определенного поля MERGEFIELD. Значение по умолчанию — 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | Указывает предопределенное имя поля слияния, которое должно быть сопоставлено с номером столбца , указанным[`Column`](./column/) свойство в этом сопоставлении полей. Значение по умолчанию — пустая строка. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан в[`Column`](./column/)property. Значение по умолчанию — пустая строка. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | Указывает, сопоставлено ли данное поле слияния почты со столбцом в данном внешнем источнике данных или нет. Значение по умолчанию:Default . |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | Возвращает глубокую копию этого объекта. |

## Примечания

Microsoft Word предоставляет некоторые предопределенные имена полей слияния, которые можно вставлять в документ как MERGEFIELD или , используя поля ADDRESSBLOCK или GREETINGLINE. Информация, указанная в`OdsoFieldMapData` позволяет сопоставить один столбец во внешнем источнике данных с одним предопределенным полем слияния.

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

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
