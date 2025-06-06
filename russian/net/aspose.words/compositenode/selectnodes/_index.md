---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words для .NET
description: Легко извлекайте узлы с помощью метода CompositeNode SelectNodes, используя выражения XPath для улучшенной обработки данных и оптимизированного кодирования.
type: docs
weight: 210
url: /ru/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

Выбирает список узлов, соответствующих выражению XPath.

```csharp
public NodeList SelectNodes(string xpath)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| xpath | String | Выражение XPath. |

### Возвращаемое значение

Список узлов, соответствующих запросу XPath.

## Примечания

В данный момент поддерживаются только выражения с именами элементов. Выражения , использующие имена атрибутов, не поддерживаются.

## Примеры

Показывает, как использовать выражение XPath для проверки того, находится ли узел внутри поля.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// NodeList, полученный в результате этого выражения XPath, будет содержать все узлы, которые мы найдем внутри поля.
// Однако узлы FieldStart и FieldEnd могут быть в списке, если в пути есть вложенные поля.
// В настоящее время не находит редкие поля, в которых FieldCode или FieldResult охватывает несколько абзацев.
NodeList resultList =
    doc.SelectNodes("//FieldStart/следующий-родственный::node()[следующий-родственный::FieldEnd]");

// Проверяем, является ли указанный запуск одним из узлов, находящихся внутри поля.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
