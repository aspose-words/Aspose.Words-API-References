---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: Легко перебирайте NodeList с помощью метода GetEnumerator. Наслаждайтесь простым и эффективным доступом к вашей коллекции узлов в C#.
type: docs
weight: 30
url: /ru/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Обеспечивает простую итерацию в стиле «foreach» по коллекции узлов.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Возвращаемое значение

IEnumerator.

## Примеры

Показывает, как выбрать определенные узлы с помощью выражения XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Это выражение извлечет все узлы абзаца,
// которые являются потомками любого узла таблицы в документе.
NodeList nodeList = doc.SelectNodes("//Таблица//Абзац");

// Проходим по списку с помощью перечислителя и выводим содержимое каждого абзаца в каждой ячейке таблицы.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Это выражение выберет все абзацы, которые являются прямыми дочерними элементами любого узла Body в документе.
nodeList = doc.SelectNodes("//Тело/Абзац");

// Мы можем рассматривать список как массив.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Используйте SelectSingleNode для выбора первого результата того же выражения, что и выше.
Node node = doc.SelectSingleNode("//Тело/Абзац");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Смотрите также

* class [Node](../../node/)
* class [NodeList](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
