---
title: CustomXmlPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получайте доступ к определенным свойствам без усилий с помощью CustomXmlPropertyCollection. Извлекайте элементы по имени для оптимизированного управления данными и повышения производительности.
type: docs
weight: 20
url: /ru/net/aspose.words.markup/customxmlpropertycollection/item/
---
## CustomXmlPropertyCollection indexer (1 of 2)

Получает свойство с указанным именем.

```csharp
public CustomXmlProperty this[string name] { get; }
```

| Параметр | Описание |
| --- | --- |
| name | Имя свойства, которое необходимо найти, чувствительно к регистру. |

## Примеры

Показывает, как работать со свойствами смарт-тегов, чтобы получить подробную информацию о смарт-тегах.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Смарт-тег появляется в документе, в котором Microsoft Word распознает часть текста как некоторую форму данных,
// например имя, дату или адрес, и преобразует его в гиперссылку, которая отображается подчеркиванием из фиолетовых точек.
// В Word 2003 мы можем включить смарт-теги через «Сервис» -> «Параметры автозамены...» -> «SmartTags».
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

* class [CustomXmlProperty](../../customxmlproperty/)
* class [CustomXmlPropertyCollection](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)

---

## CustomXmlPropertyCollection indexer (2 of 2)

Получает свойство по указанному индексу.

```csharp
public CustomXmlProperty this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс недвижимости, отсчитываемый от нуля. |

## Примеры

Показывает, как работать со свойствами смарт-тегов, чтобы получить подробную информацию о смарт-тегах.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Смарт-тег появляется в документе, в котором Microsoft Word распознает часть текста как некоторую форму данных,
// например имя, дату или адрес, и преобразует его в гиперссылку, которая отображается подчеркиванием из фиолетовых точек.
// В Word 2003 мы можем включить смарт-теги через «Сервис» -> «Параметры автозамены...» -> «SmartTags».
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

* class [CustomXmlProperty](../../customxmlproperty/)
* class [CustomXmlPropertyCollection](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
