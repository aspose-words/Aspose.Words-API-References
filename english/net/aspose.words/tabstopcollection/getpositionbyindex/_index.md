---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words for .NET
description: Discover the TabStopCollection GetPositionByIndex method to easily find tab stop positions in points by index. Optimize your layout effortlessly!
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
Assert.That(tabStops.GetPositionByIndex(1), Is.EqualTo(ConvertUtil.MillimeterToPoint(60)).Within(0.1d));
```

### See Also

* class [TabStopCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
