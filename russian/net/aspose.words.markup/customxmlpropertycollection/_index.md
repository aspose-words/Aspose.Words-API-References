---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Markup.CustomXmlPropertyCollection — мощный инструмент для эффективного управления пользовательскими атрибутами XML и свойствами смарт-тегов.
type: docs
weight: 4640
url: /ru/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Представляет коллекцию пользовательских атрибутов XML или свойств смарт-тегов.

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Получает свойство с указанным именем. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Добавляет свойство в коллекцию. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Удаляет все элементы из коллекции. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Определяет, содержит ли коллекция свойство с указанным именем. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Возвращает отсчитываемый от нуля индекс указанного свойства в коллекции. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Удаляет свойство с указанным именем из коллекции. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Удаляет свойство по указанному индексу. |

## Примечания

Элементы есть[`CustomXmlProperty`](../customxmlproperty/) объекты.

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

* class [CustomXmlProperty](../customxmlproperty/)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
