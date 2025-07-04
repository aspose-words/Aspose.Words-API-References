---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words for .NET
description: Effortlessly manage your tab stops with the RemoveByIndex method. Quickly remove any tab stop from your collection for streamlined design.
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

Assert.That(tabStops.Count, Is.EqualTo(2));

// Remove the first tab stop.
tabStops.RemoveByIndex(0);

Assert.That(tabStops.Count, Is.EqualTo(1));

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### See Also

* class [TabStopCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
