---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words for .NET
description: Discover how CompositeNode's SelectSingleNode method efficiently retrieves the first Node matching your XPath expression for streamlined data handling.
type: docs
weight: 220
url: /net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

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
Assert.That(nodeList.ToArray().Length, Is.EqualTo(4));

// Use SelectSingleNode to select the first result of the same expression as above.
Node node = doc.SelectSingleNode("//Body/Paragraph");

Assert.That(node.GetType(), Is.EqualTo(typeof(Paragraph)));
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
