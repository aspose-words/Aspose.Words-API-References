---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BaseWebExtensionCollection Item для простого управления элементами по индексу. Упростите свою разработку с помощью эффективной обработки данных уже сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Получает или задает элемент по указанному индексу.

```csharp
public T this[int index] { get; set; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс элемента, отсчитываемый от нуля. |

## Примеры

Показывает, как работать с коллекцией веб-расширений документа.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Распечатать все свойства веб-расширения документа.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Удалить веб-расширение.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Смотрите также

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* пространство имен [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* сборка [Aspose.Words](../../../)
