---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
second_title: Aspose.Words for .NET API Reference
description: CompositeNode SelectSingleNode method. Selects the first Node that matches the XPath expression in C#.
type: docs
weight: 210
url: /net/aspose.words/compositenode/selectsinglenode/
---
## SelectSingleNode method

Selects the first [`Node`](../../node/) that matches the XPath expression.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | String | The XPath expression. |

### Return Value

The first [`Node`](../../node/) that matches the XPath query or `null` if no matching node is found.

## Remarks

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

## Examples

Shows how to select certain nodes by using an XPath expression.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// This expression will extract all paragraph nodes,
// which are descendants of any table node in the document.
NodeList nodeList = doc.SelectNodes("//Table//Paragraph");

// Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// This expression will select any paragraphs that are direct children of any Body node in the document.
nodeList = doc.SelectNodes("//Body/Paragraph");

// We can treat the list as an array.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Use SelectSingleNode to select the first result of the same expression as above.
Node node = doc.SelectSingleNode("//Body/Paragraph");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
