---
title: TabStopCollection
linktitle: TabStopCollection
second_title: Aspose.Words for Java
description: A collection of TabStop objects that represent custom tabs for a paragraph or a style in Java.
type: docs
weight: 583
url: /java/com.aspose.words/tabstopcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

A collection of [TabStop](../../com.aspose.words/tabstop/) objects that represent custom tabs for a paragraph or a style.

To learn more, visit the [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] documentation article.

 **Remarks:** 

In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph style or directly in the properties of a paragraph. A style can be based on another style. Therefore, the complete set of tab stops for a given object is a combination of tab stops defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a [TabStopCollection](../../com.aspose.words/tabstopcollection/) for a paragraph or a style, it contains only the custom tab stops defined directly for this paragraph or style. The collection does not include tab stops defined in the parent styles or default tab stops.

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Methods

| Method | Description |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop) | Adds or replaces a tab stop in the collection. |
| [add(double position, int alignment, int leader)](#add-double-int-int) |  |
| [after(double position)](#after-double) | Gets a first tab stop to the right of the specified position. |
| [before(double position)](#before-double) | Gets a first tab stop to the left of the specified position. |
| [clear()](#clear) | Deletes all tab stop positions. |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection) | Determines whether the specified [TabStopCollection](../../com.aspose.words/tabstopcollection/) is equal in value to the current [TabStopCollection](../../com.aspose.words/tabstopcollection/). |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [get(double position)](#get-double) | Gets a tab stop at the specified position. |
| [get(int index)](#get-int) | Retrieves a tab stop from the collection. |
| [getCount()](#getCount) | Gets the number of tab stops in the collection. |
| [getIndexByPosition(double position)](#getIndexByPosition-double) | Gets the index of a tab stop with the specified position in points. |
| [getPositionByIndex(int index)](#getPositionByIndex-int) | Gets the position (in points) of the tab stop at the specified index. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [removeByIndex(int index)](#removeByIndex-int) | Removes a tab stop at the specified index from the collection. |
| [removeByPosition(double position)](#removeByPosition-double) | Removes a tab stop at the specified position from the collection. |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop}
```
public void add(TabStop tabStop)
```


Adds or replaces a tab stop in the collection.

 **Remarks:** 

If a tab stop already exists at the specified position, it is replaced.

 **Examples:** 

Shows how to add custom tab stops to a document.

```

 Document doc = new Document();
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);

 // Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
 // 1 -  Create a "TabStop" object, and then add it to the collection:
 TabStop tabStop = new TabStop(ConvertUtil.inchToPoint(3.0), TabAlignment.LEFT, TabLeader.DASHES);
 paragraph.getParagraphFormat().getTabStops().add(tabStop);

 // 2 -  Pass the values for properties of a new tab stop to the "Add" method:
 paragraph.getParagraphFormat().getTabStops().add(ConvertUtil.millimeterToPoint(100.0), TabAlignment.LEFT,
         TabLeader.DASHES);

 // Add tab stops at 5 cm to all paragraphs.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     para.getParagraphFormat().getTabStops().add(ConvertUtil.millimeterToPoint(50.0), TabAlignment.LEFT,
             TabLeader.DASHES);
 }

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

 doc.save(getArtifactsDir() + "TabStopCollection.AddTabStops.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop/) | A tab stop object to add. |

### add(double position, int alignment, int leader) {#add-double-int-int}
```
public void add(double position, int alignment, int leader)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### after(double position) {#after-double}
```
public TabStop after(double position)
```


Gets a first tab stop to the right of the specified position.

 **Remarks:** 

Skips tab stops with [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) set to [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### before(double position) {#before-double}
```
public TabStop before(double position)
```


Gets a first tab stop to the left of the specified position.

 **Remarks:** 

Skips tab stops with [TabStop.getAlignment()](../../com.aspose.words/tabstop/\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop/\#setAlignment-int) set to [TabAlignment.BAR](../../com.aspose.words/tabalignment/\#BAR).

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop object or  null  if a suitable tab stop was not found.
### clear() {#clear}
```
public void clear()
```


Deletes all tab stop positions.

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection}
```
public boolean equals(TabStopCollection rhs)
```


Determines whether the specified [TabStopCollection](../../com.aspose.words/tabstopcollection/) is equal in value to the current [TabStopCollection](../../com.aspose.words/tabstopcollection/).

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### get(double position) {#get-double}
```
public TabStop get(double position)
```


Gets a tab stop at the specified position.

 **Remarks:** 

Returns  null  if no tab stop is found at the specified position.

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - A tab stop at the specified position.
### get(int index) {#get-int}
```
public TabStop get(int index)
```


Retrieves a tab stop from the collection.  Gets a tab stop at the given index.

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop/) - The corresponding [TabStop](../../com.aspose.words/tabstop/) value.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of tab stops in the collection.

 **Examples:** 

Shows how to work with a document's collection of tab stops.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TabStopCollection tabStops = builder.getParagraphFormat().getTabStops();

 // 72 points is one "inch" on the Microsoft Word tab stop ruler.
 tabStops.add(new TabStop(72.0));
 tabStops.add(new TabStop(432, TabAlignment.RIGHT, TabLeader.DASHES));

 Assert.assertEquals(2, tabStops.getCount());
 Assert.assertFalse(tabStops.get(0).isClear());
 Assert.assertFalse(tabStops.get(0).equals(tabStops.get(1)));

 // Every "tab" character takes the builder's cursor to the location of the next tab stop.
 builder.writeln("Start\tTab 1\tTab 2");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(2, paragraphs.getCount());

 // Each paragraph gets its tab stop collection, which clones its values from the document builder's tab stop collection.
 Assert.assertEquals(paragraphs.get(0).getParagraphFormat().getTabStops(), paragraphs.get(1).getParagraphFormat().getTabStops());

 // A tab stop collection can point us to TabStops before and after certain positions.
 Assert.assertEquals(72.0, tabStops.before(100.0).getPosition());
 Assert.assertEquals(432.0, tabStops.after(100.0).getPosition());

 // We can clear a paragraph's tab stop collection to revert to the default tabbing behavior.
 paragraphs.get(1).getParagraphFormat().getTabStops().clear();

 Assert.assertEquals(0, paragraphs.get(1).getParagraphFormat().getTabStops().getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.TabStopCollection.docx");
 
```

**Returns:**
int - The number of tab stops in the collection.
### getIndexByPosition(double position) {#getIndexByPosition-double}
```
public int getIndexByPosition(double position)
```


Gets the index of a tab stop with the specified position in points.

 **Examples:** 

Shows how to look up a position to see if a tab stop exists there and obtain its index.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 // Add a tab stop at a position of 30mm.
 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);

 // A result of "0" returned by "GetIndexByPosition" confirms that a tab stop
 // at 30mm exists in this collection, and it is at index 0.
 Assert.assertEquals(0, tabStops.getIndexByPosition(ConvertUtil.millimeterToPoint(30.0)));

 // A "-1" returned by "GetIndexByPosition" confirms that
 // there is no tab stop in this collection with a position of 60mm.
 Assert.assertEquals(-1, tabStops.getIndexByPosition(ConvertUtil.millimeterToPoint(60.0)));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |

**Returns:**
int
### getPositionByIndex(int index) {#getPositionByIndex-int}
```
public double getPositionByIndex(int index)
```


Gets the position (in points) of the tab stop at the specified index.

 **Examples:** 

Shows how to find a tab, stop by its index and verify its position.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);
 tabStops.add(ConvertUtil.millimeterToPoint(60.0), TabAlignment.LEFT, TabLeader.DASHES);

 // Verify the position of the second tab stop in the collection.
 Assert.assertEquals(ConvertUtil.millimeterToPoint(60.0), tabStops.getPositionByIndex(1), 0.1d);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

**Returns:**
double - The position of the tab stop.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### removeByIndex(int index) {#removeByIndex-int}
```
public void removeByIndex(int index)
```


Removes a tab stop at the specified index from the collection.

 **Examples:** 

Shows how to select a tab stop in a document by its index and remove it.

```

 Document doc = new Document();
 TabStopCollection tabStops = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getTabStops();

 tabStops.add(ConvertUtil.millimeterToPoint(30.0), TabAlignment.LEFT, TabLeader.DASHES);
 tabStops.add(ConvertUtil.millimeterToPoint(60.0), TabAlignment.LEFT, TabLeader.DASHES);

 Assert.assertEquals(2, tabStops.getCount());

 // Remove the first tab stop.
 tabStops.removeByIndex(0);

 Assert.assertEquals(1, tabStops.getCount());

 doc.save(getArtifactsDir() + "TabStopCollection.RemoveByIndex.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

### removeByPosition(double position) {#removeByPosition-double}
```
public void removeByPosition(double position)
```


Removes a tab stop at the specified position from the collection.

 **Examples:** 

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop to remove. |

