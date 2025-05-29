---
title: OdsoRecipientDataCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Легко управляйте OdsoRecipientDataCollection с помощью нашего свойства Item. Легко извлекайте или обновляйте элементы для бесперебойной обработки данных.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/odsorecipientdatacollection/item/
---
## OdsoRecipientDataCollection indexer

Получает или задает элемент в этой коллекции.

```csharp
public OdsoRecipientData this[int index] { get; set; }
```

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

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
