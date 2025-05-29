---
title: OdsoRecipientData.Column
linktitle: Column
articleTitle: Column
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OdsoRecipientData Column, легко идентифицируйте уникальные столбцы данных для записей, улучшая управление данными. Значение по умолчанию — 0.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/odsorecipientdata/column/
---
## OdsoRecipientData.Column property

Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. Значение по умолчанию — 0.

```csharp
public int Column { get; set; }
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

* class [OdsoRecipientData](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
