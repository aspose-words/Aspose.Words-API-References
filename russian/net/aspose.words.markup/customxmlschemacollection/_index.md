---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Markup.CustomXmlSchemaCollection для управления схемами XML, связанными с пользовательскими частями XML, что повышает гибкость и контроль над документами.
type: docs
weight: 4650
url: /ru/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Коллекция строк, представляющих схемы XML, связанные с пользовательской частью XML.

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Получает или задает элемент по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | Добавляет элемент в коллекцию. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Удаляет все элементы из коллекции. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Создает глубокую копию этого объекта. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | Возвращает отсчитываемый от нуля индекс указанного значения в коллекции. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | Удаляет указанное значение из коллекции. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | Удаляет значение по указанному индексу. |

## Примечания

Вы не создаете экземпляры этого класса. Вы получаете доступ к коллекции XML-схем пользовательского XML part через[`Schemas`](../customxmlpart/schemas/) свойство.

## Примеры

Показывает, как работать с коллекцией XML-схем.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Добавить ассоциацию схемы XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Клонировать коллекцию ассоциаций XML-схемы пользовательской XML-части,
// а затем добавляем в клон пару новых схем.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Перечислить схемы и вывести каждый элемент.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Ниже приведены три способа удаления схем из коллекции.
// 1 - Удалить схему по индексу:
schemas.RemoveAt(2);

// 2 - Удалить схему по значению:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Используйте метод «Очистить», чтобы очистить коллекцию сразу.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
