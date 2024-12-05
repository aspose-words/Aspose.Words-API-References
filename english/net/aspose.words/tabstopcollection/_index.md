---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.TabStopCollection class. A collection of TabStop objects that represent custom tabs for a paragraph or a style in C#.
type: docs
weight: 6860
url: /net/aspose.words/tabstopcollection/
---
## TabStopCollection class

A collection of [`TabStop`](../tabstop/) objects that represent custom tabs for a paragraph or a style.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Gets the number of tab stops in the collection. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Gets a tab stop at the given index. (2 indexers) |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Adds or replaces a tab stop in the collection. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Adds or replaces a tab stop in the collection. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Gets a first tab stop to the right of the specified position. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Gets a first tab stop to the left of the specified position. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Deletes all tab stop positions. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Determines whether the specified object is equal in value to the current object. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Determines whether the specified `TabStopCollection` is equal in value to the current `TabStopCollection`. |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Serves as a hash function for this type. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Gets the index of a tab stop with the specified position in points. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Gets the position (in points) of the tab stop at the specified index. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Removes a tab stop at the specified index from the collection. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Removes a tab stop at the specified position from the collection. |

## Remarks

In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph style or directly in the properties of a paragraph. A style can be based on another style. Therefore, the complete set of tab stops for a given object is a combination of tab stops defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a `TabStopCollection` for a paragraph or a style, it contains only the custom tab stops defined directly for this paragraph or style. The collection does not include tab stops defined in the parent styles or default tab stops.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
