---
title: GetHashCode
second_title: Aspose.Words for .NET API Reference
description: TabStopCollection method. Serves as a hash function for this type in C#.
type: docs
weight: 80
url: /net/aspose.words/tabstopcollection/gethashcode/
---
## TabStopCollection.GetHashCode method

Serves as a hash function for this type.

```csharp
public override int GetHashCode()
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

* class [TabStopCollection](../)
* namespace [Aspose.Words](../../tabstopcollection/)
* assembly [Aspose.Words](../../../)
