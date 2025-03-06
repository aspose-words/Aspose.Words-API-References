---
title: TabStop
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words for .NET
description: Discover TabStop constructor, effortlessly create and customize instances for enhanced functionality in your projects. Boost your coding efficiency today!
type: docs
weight: 10
url: /net/aspose.words/tabstop/tabstop/
---
## TabStop(*double*) {#constructor}

Initializes a new instance of this class.

```csharp
public TabStop(double position)
```

## Examples

Shows how to work with a document's collection of tab stops.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 points is one "inch" on the Microsoft Word tab stop ruler.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// A tab stop collection can point us to TabStops before and after certain positions.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### See Also

* class [TabStop](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## TabStop(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#constructor_1}

Initializes a new instance of this class.

```csharp
public TabStop(double position, TabAlignment alignment, TabLeader leader)
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | Double | The position of the tab stop in points. |
| alignment | TabAlignment | A [`TabAlignment`](../../tabalignment/) value that specifies the alignment of text at this tab stop. |
| leader | TabLeader | A [`TabLeader`](../../tableader/) value that specifies the type of the leader line displayed under the tab character. |

## Examples

Shows how to work with a document's collection of tab stops.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 points is one "inch" on the Microsoft Word tab stop ruler.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// A tab stop collection can point us to TabStops before and after certain positions.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### See Also

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
