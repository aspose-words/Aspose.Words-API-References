---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: Discover how the TabStopCollection Add method efficiently adds or updates tab stops, enhancing your document's layout and formatting.
type: docs
weight: 30
url: /net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

Adds or replaces a tab stop in the collection.

```csharp
public void Add(TabStop tabStop)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tabStop | TabStop | A tab stop object to add. |

## Remarks

If a tab stop already exists at the specified position, it is replaced.

## Examples

Shows how to add custom tab stops to a document.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
// 1 -  Create a "TabStop" object, and then add it to the collection:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 -  Pass the values for properties of a new tab stop to the "Add" method:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Add tab stops at 5 cm to all paragraphs.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### See Also

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

Adds or replaces a tab stop in the collection.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | Double | A position (in points) where to add the tab stop. |
| alignment | TabAlignment | A [`TabAlignment`](../../tabalignment/) value that specifies the alignment of text at the tab stop. |
| leader | TabLeader | A [`TabLeader`](../../tableader/) value that specifies the type of the leader line displayed under the tab character. |

## Remarks

If a tab stop already exists at the specified position, it is replaced.

## Examples

Shows how to add custom tab stops to a document.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
// 1 -  Create a "TabStop" object, and then add it to the collection:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 -  Pass the values for properties of a new tab stop to the "Add" method:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Add tab stops at 5 cm to all paragraphs.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### See Also

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
