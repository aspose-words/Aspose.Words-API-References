---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: Откройте для себя метод BaseWebExtensionCollection GetEnumerator для легкой итерации коллекций, повышения эффективности разработки и управления кодом.
type: docs
weight: 50
url: /ru/net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## BaseWebExtensionCollection&lt;T&gt;.GetEnumerator method

Возвращает перечислитель, который может выполнять итерацию по коллекции.

```csharp
public IEnumerator<T> GetEnumerator()
```

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
