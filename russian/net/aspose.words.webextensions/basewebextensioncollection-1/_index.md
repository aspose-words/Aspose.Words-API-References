---
title: BaseWebExtensionCollectionT Class
linktitle: BaseWebExtensionCollectionT
articleTitle: BaseWebExtensionCollectionT
second_title: Aspose.Words для .NET
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T сорт. Базовый класс дляTaskPaneCollection WebExtensionBindingCollection  WebExtensionPropertyCollection иWebExtensionReferenceCollection коллекции на С#.
type: docs
weight: 6700
url: /ru/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Базовый класс для[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) и[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) коллекции.

Чтобы узнать больше, посетите[Работа с надстройками Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) статья документации.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Параметр | Описание |
| --- | --- |
| T | Тип элемента коллекции. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Получает или задает элемент по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*T*) | Добавляет указанный элемент в коллекцию. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Удаляет все элементы из коллекции. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Возвращает перечислитель, который может перебирать коллекцию. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) | Удаляет элемент по указанному индексу из коллекции. |

## Примеры

Показывает, как работать с коллекцией веб-расширений документа.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Распечатываем все свойства веб-расширения документа.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Удаляем веб-расширение.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* сборка [Aspose.Words](../../)
