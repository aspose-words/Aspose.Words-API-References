---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words for .NET API Reference
description: TabStopCollection RemoveByIndex method. Removes a tab stop at the specified index from the collection in C#.
type: docs
weight: 110
url: /net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Removes a tab stop at the specified index from the collection.

```csharp
public void RemoveByIndex(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | An index into the collection of tab stops. |

## Examples

Shows how to select a tab stop in a document by its index and remove it.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// Remove the first tab stop.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### See Also

* class [TabStopCollection](../)
* namespace [Aspose.Words](../../tabstopcollection/)
* assembly [Aspose.Words](../../../)
