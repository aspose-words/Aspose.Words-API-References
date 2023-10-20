---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words для .NET
description: CompositeNode SelectSingleNode метод. Выбирает первыйNode которое соответствует выражению XPath на С#.
type: docs
weight: 200
url: /ru/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Выбирает первый[`Node`](../../node/) которое соответствует выражению XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | String | Выражение XPath. |

### Возвращаемое значение

Первый[`Node`](../../node/) который соответствует запросу XPath или`нулевой` если соответствующий узел не найден.

## Примечания

На данный момент поддерживаются только выражения с именами элементов. Выражения , использующие имена атрибутов, не поддерживаются.

## Примеры

Показывает, как выбрать определенные узлы с помощью выражения XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Это выражение извлечет все узлы абзаца,
// которые являются потомками любого узла таблицы в документе.
NodeList nodeList = doc.SelectNodes("//Таблица//Абзац");

// Перебираем список с помощью перечислителя и печатаем содержимое каждого абзаца в каждой ячейке таблицы.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Это выражение выберет любые абзацы, которые являются прямыми дочерними элементами любого узла Body в документе.
nodeList = doc.SelectNodes("//Тело/Абзац");

// Мы можем рассматривать список как массив.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Используйте SelectSingleNode, чтобы выбрать первый результат того же выражения, что и выше.
Node node = doc.SelectSingleNode("//Тело/Абзац");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Смотрите также

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
