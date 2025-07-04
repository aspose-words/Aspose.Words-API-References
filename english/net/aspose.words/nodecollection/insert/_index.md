---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words for .NET
description: Effortlessly insert nodes into your NodeCollection at any index with our streamlined Insert method. Enhance your data management today!
type: docs
weight: 80
url: /net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Inserts a node into the collection at the specified index.

```csharp
public void Insert(int index, Node node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | Node | The node to insert. |

### Exceptions

| exception | condition |
| --- | --- |
| NotSupportedException | The [`NodeCollection`](../) is a "deep" collection. |

## Remarks

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than [`Count`](../count/), the node is added at the end of the collection.

If the index is negative and its absolute value is greater than [`Count`](../count/), the node is added at the end of the collection.

If the node being inserted was created from another document, you should use [`ImportNode`](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.

## Examples

Shows how to work with a NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add text to the document by inserting Runs using a DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Every invocation of the "Write" method creates a new Run,
// which then appears in the parent Paragraph's RunCollection.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.That(runs.Count, Is.EqualTo(2));

// We can also insert a node into the RunCollection manually.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.That(runs.Contains(newRun), Is.True);
Assert.That(doc.GetText().Trim(), Is.EqualTo("Run 1. Run 2. Run 3."));

// Access individual runs and remove them to remove their text from the document.
Run run = runs[1];
runs.Remove(run);

Assert.That(doc.GetText().Trim(), Is.EqualTo("Run 1. Run 3."));
Assert.That(run, Is.Not.Null);
Assert.That(runs.Contains(run), Is.False);
```

### See Also

* class [Node](../../node/)
* class [NodeCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
