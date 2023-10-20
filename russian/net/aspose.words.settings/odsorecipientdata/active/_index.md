---
title: OdsoRecipientData.Active
linktitle: Active
articleTitle: Active
second_title: Aspose.Words для .NET
description: OdsoRecipientData Active свойство. Указывает должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. Значение по умолчаниюистинный  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.settings/odsorecipientdata/active/
---
## OdsoRecipientData.Active property

Указывает, должна ли запись из источника данных быть импортирована в документ при выполнении слияния почты. Значение по умолчанию:`истинный` .

```csharp
public bool Active { get; set; }
```

## Примеры

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

* class [OdsoRecipientData](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
