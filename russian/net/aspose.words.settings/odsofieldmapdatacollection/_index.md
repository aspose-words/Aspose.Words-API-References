---
title: Class OdsoFieldMapDataCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Settings.OdsoFieldMapDataCollection сорт. Типизированная коллекцияOdsoFieldMapData объекты.
type: docs
weight: 5910
url: /ru/net/aspose.words.settings/odsofieldmapdatacollection/
---
## OdsoFieldMapDataCollection class

Типизированная коллекция[`OdsoFieldMapData`](../odsofieldmapdata/) объекты.

Чтобы узнать больше, посетите[Слияние почты и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) статья документации.

```csharp
public class OdsoFieldMapDataCollection : IEnumerable<OdsoFieldMapData>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OdsoFieldMapDataCollection](odsofieldmapdatacollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.settings/odsofieldmapdatacollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.settings/odsofieldmapdatacollection/item/) { get; set; } | Получает или задает элемент в этой коллекции. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.settings/odsofieldmapdatacollection/add/)(OdsoFieldMapData) | Добавляет объект в конец этой коллекции. |
| [Clear](../../aspose.words.settings/odsofieldmapdatacollection/clear/)() | Удаляет все элементы из этой коллекции. |
| [GetEnumerator](../../aspose.words.settings/odsofieldmapdatacollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов коллекции. |
| [RemoveAt](../../aspose.words.settings/odsofieldmapdatacollection/removeat/)(int) | Удаляет элемент по указанному индексу. |

### Примеры

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

* class [OdsoFieldMapData](../odsofieldmapdata/)
* property [FieldMapDatas](../odso/fieldmapdatas/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)


