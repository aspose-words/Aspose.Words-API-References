---
title: GetPositionByIndex
second_title: Aspose.Words for .NET API Reference
description: TabStopCollection method. Gets the position in points of the tab stop at the specified index in C#.
type: docs
weight: 100
url: /net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Gets the position (in points) of the tab stop at the specified index.

```csharp
public double GetPositionByIndex(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | An index into the collection of tab stops. |

### Return Value

The position of the tab stop.

## Examples

Shows how to find a tab, stop by its index and verify its position.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Verify the position of the second tab stop in the collection.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### See Also

* class [TabStopCollection](../)
* namespace [Aspose.Words](../../tabstopcollection/)
* assembly [Aspose.Words](../../../)
