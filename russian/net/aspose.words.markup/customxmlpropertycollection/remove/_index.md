---
title: CustomXmlPropertyCollection.Remove
second_title: Справочник по API Aspose.Words для .NET
description: CustomXmlPropertyCollection метод. Удаляет свойство с указанным именем из коллекции.
type: docs
weight: 80
url: /ru/net/aspose.words.markup/customxmlpropertycollection/remove/
---
## CustomXmlPropertyCollection.Remove method

Удаляет свойство с указанным именем из коллекции.

```csharp
public void Remove(string name)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя свойства с учетом регистра. |

### Примеры

Показывает, как работать со свойствами смарт-тегов, чтобы получить подробную информацию о смарт-тегах.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Смарт-тег появляется в документе, когда Microsoft Word распознает часть его текста как некоторую форму данных,
// например, имя, дата или адрес, и преобразует его в гиперссылку, подчеркнутую фиолетовым пунктиром.
// В Word 2003 мы можем включить смарт-теги через «Инструменты» -> > "Параметры автозамены..." -> «СмартТеги».
// В нашем входном документе есть три объекта, которые Microsoft Word зарегистрировал как смарт-теги.
// Смарт-теги могут быть вложенными, поэтому эта коллекция содержит больше.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Элемент «Свойства» смарт-тега содержит его метаданные, которые будут разными для каждого типа смарт-тега.
// Свойства смарт-тега типа «дата» содержат год, месяц и день.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Мы также можем получить доступ к свойствам различными способами, например, с помощью пары ключ-значение.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Ниже приведены три способа удаления элементов из коллекции свойств.
// 1 - Удалить по индексу:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Удалить по имени:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Очистить всю коллекцию сразу:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Смотрите также

* class [CustomXmlPropertyCollection](../)
* пространство имен [Aspose.Words.Markup](../../customxmlpropertycollection/)
* сборка [Aspose.Words](../../../)


