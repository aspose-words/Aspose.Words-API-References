---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words for .NET
description: Discover the TabStopCollection GetIndexByPosition method to easily find the index of a tab stop at any specified point position. Perfect for precise layout control!
type: docs
weight: 90
url: /net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Gets the index of a tab stop with the specified position in points.

```csharp
public int GetIndexByPosition(double position)
```

## Examples

Shows how to look up a position to see if a tab stop exists there and obtain its index.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Add a tab stop at a position of 30mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// A result of "0" returned by "GetIndexByPosition" confirms that a tab stop
// at 30mm exists in this collection, and it is at index 0.
Assert.That(tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)), Is.EqualTo(0));

// A "-1" returned by "GetIndexByPosition" confirms that
// there is no tab stop in this collection with a position of 60mm.
Assert.That(tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)), Is.EqualTo(-1));
```

### See Also

* class [TabStopCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
