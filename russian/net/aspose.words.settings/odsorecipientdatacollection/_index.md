---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Settings.OdsoRecipientDataCollection — мощную типизированную коллекцию для эффективного управления OdsoRecipientData в ваших приложениях.
type: docs
weight: 6770
url: /ru/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

Типизированная коллекция[`OdsoRecipientData`](../odsorecipientdata/)

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | Получает или задает элемент в этой коллекции. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | Добавляет объект в конец этой коллекции. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | Удаляет все элементы из этой коллекции. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | Удаляет элемент по указанному индексу. |

## Примеры

Показывает, как получить доступ к набору данных, определяющему, какие записи источников данных слияния будут исключены при слиянии почты.

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

* class [OdsoRecipientData](../odsorecipientdata/)
* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
