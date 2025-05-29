---
title: CustomXmlSchemaCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Узнайте, как легко управлять элементами CustomXmlSchemaCollection. Узнайте, как получать или задавать элементы по индексу для упрощенной обработки XML-данных.
type: docs
weight: 20
url: /ru/net/aspose.words.markup/customxmlschemacollection/item/
---
## CustomXmlSchemaCollection indexer

Получает или задает элемент по указанному индексу.

```csharp
public string this[int index] { get; set; }
```

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

* class [CustomXmlSchemaCollection](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
