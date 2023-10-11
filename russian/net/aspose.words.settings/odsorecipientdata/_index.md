---
title: Class OdsoRecipientData
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Settings.OdsoRecipientData сорт. Представляет информацию об одной записи во внешнем источнике данных которая должна быть исключена из слияния почты.
type: docs
weight: 5930
url: /ru/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Представляет информацию об одной записи во внешнем источнике данных, которая должна быть исключена из слияния почты.

Чтобы узнать больше, посетите[Слияние почты и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) статья документации.

```csharp
public class OdsoRecipientData
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | Указывает, должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. Значение по умолчанию:`истинный` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | Указывает столбец в источнике данных, который содержит уникальные данные для текущей записи. Значение по умолчанию: 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | Представляет хэш-код этой записи. Иногда Microsoft Word использует[`Hash`](./hash/) всей записи вместо[`UniqueTag`](./uniquetag/) value. Значение по умолчанию — 0. . |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию:`нулевой` . |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | Возвращает глубокую копию этого объекта. |

### Примечания

Если запись должна быть объединена в объединенный документ, то никакой информации об этой записи не требуется. Однако, если данная запись не должна быть объединена в объединенный документ, то значение уникального ключа для этой записи должно храниться в[`UniqueTag`](./uniquetag/)свойство этого объекта, чтобы указать это исключение.

### Примеры

Показывает, как получить доступ к коллекции данных, определяющей, какие записи источника данных слияния будут исключены при слиянии почты.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Мы можем клонировать элементы этой коллекции.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Мы также можем удалить элементы по отдельности или очистить всю коллекцию сразу.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)


