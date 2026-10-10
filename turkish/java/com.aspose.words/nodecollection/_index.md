---
title: "NodeCollection"
linktitle: "NodeCollection"
second_title: "Aspose.Words Java için"
description: "Java'da belirli bir türdeki düğümlerin bir koleksiyonunu temsil eder."
type: docs
weight: 479
url: /tr/java/com.aspose.words/nodecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class NodeCollection implements Iterable
```

Belirli bir türdeki düğümlerin bir koleksiyonunu temsil eder.

Daha fazla bilgi edinmek için, [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[NodeCollection](../../com.aspose.words/nodecollection/) does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](../../com.aspose.words/nodecollection/) supports indexed access, iteration and provides add and remove methods.

Bu [NodeCollection](../../com.aspose.words/nodecollection/) koleksiyonu "canlı"dır, yani oluşturulduğu düğüm nesnesinin çocuklarında yapılan değişiklikler, [NodeCollection](../../com.aspose.words/nodecollection/) özellikleri ve yöntemleri tarafından döndürülen düğümlerde anında yansır.

[NodeCollection](../../com.aspose.words/nodecollection/) is returned by **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** and also serves as a base class for typed node collections such as [SectionCollection](../../com.aspose.words/sectioncollection/), [ParagraphCollection](../../com.aspose.words/paragraphcollection/) etc.

[NodeCollection](../../com.aspose.words/nodecollection/) can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

 **Examples:** 

Tüm metin kutusu şekillerinin nasıl görüntü şekilleriyle değiştirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Bir düğümü koleksiyonun sonuna ekler. |
| [clear()](#clear) | Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [get(int index)](#get-int) | Verilen indeksdeki bir düğümü alır. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Koleksiyondaki düğüm sayısını alır. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Belirtilen düğümün sıfır tabanlı indeksini döndürür. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Belirtilen indekste bir düğümü koleksiyona ekler. |
| [iterator()](#iterator) | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [remove(Node node)](#remove-com.aspose.words.Node) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [removeAt(int index)](#removeAt-int) | Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır. |
| [toArray()](#toArray) | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Bir düğümü koleksiyonun sonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Koleksiyonun sonuna eklenecek düğüm. |

### clear() {#clear}
```
public void clear()
```


Bu koleksiyondaki ve belgedeki tüm düğümleri kaldırır.

 **Examples:** 

Bir belgede tüm bölümleri nasıl kaldıracağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // This document has one section with a few child nodes containing and displaying all the document's contents.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 Assert.assertEquals(doc.getSections().get(0).getChildNodes(NodeType.ANY, true).getCount(), 17);
 Assert.assertEquals("Hello World!\r\rHello Word!\r\r\rHello World!", doc.getText().trim());

 // Clear the collection of sections, which will remove all of the document's children.
 doc.getSections().clear();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.ANY, true).getCount());
 Assert.assertEquals("", doc.getText().trim());
 
```

### contains(Node node) {#contains-com.aspose.words.Node}
```
public boolean contains(Node node)
```


Bir düğümün koleksiyonda olup olmadığını belirler.

 **Remarks:** 

Bu yöntem doğrusal bir arama gerçekleştirir; bu nedenle, ortalama yürütme süresi [getCount()](../../com.aspose.words/nodecollection/\#getCount) ile orantılıdır.

 **Examples:** 

Bir NodeCollection ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the document by inserting Runs using a DocumentBuilder.
 builder.write("Run 1. ");
 builder.write("Run 2. ");

 // Every invocation of the "Write()" method creates a new Run,
 // which then appears in the parent Paragraph's RunCollection.
 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertEquals(2, runs.getCount());

 // We can also insert a node into the RunCollection manually.
 Run newRun = new Run(doc, "Run 3. ");
 runs.insert(3, newRun);

 Assert.assertTrue(runs.contains(newRun));
 Assert.assertEquals("Run 1. Run 2. Run 3.", doc.getText().trim());

 // Access individual runs and remove them to remove their text from the document.
 Run run = runs.get(1);
 runs.remove(run);

 Assert.assertEquals("Run 1. Run 3.", doc.getText().trim());
 Assert.assertNotNull(run);
 Assert.assertFalse(runs.contains(run));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Bulunacak düğüm. |

**Returns:**
boolean - öğe koleksiyonda bulunursa true; aksi takdirde false.
### get(int index) {#get-int}
```
public Node get(int index)
```


Verilen indeksdeki bir düğümü alır.

 **Remarks:** 

Dizin sıfır tabanlıdır.

Negatif dizinlere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi ve böyle devam eder.

Eğer dizin listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

Eğer dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

 **Examples:** 

Bir birleşik düğümün çocuk düğüm koleksiyonunda nasıl gezileceğini gösterir.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Düğümler koleksiyonundaki bir indeks. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [Node](../../com.aspose.words/node/) value.
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki düğüm sayısını alır.

 **Examples:** 

Bir birleşik düğümün çocuk düğüm koleksiyonunda nasıl gezileceğini gösterir.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

Tabloların iç içe olup olmadığını bulmayı gösterir.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Returns:**
int - koleksiyondaki düğüm sayısı.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Belirtilen düğümün sıfır tabanlı indeksini döndürür.

 **Remarks:** 

Bu yöntem doğrusal bir arama gerçekleştirir; bu nedenle, ortalama yürütme süresi [getCount()](../../com.aspose.words/nodecollection/\#getCount) ile orantılıdır.

 **Examples:** 

Bir koleksiyondaki bir düğümün dizinini nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 NodeCollection allTables = doc.getChildNodes(NodeType.TABLE, true);

 Assert.assertEquals(0, allTables.indexOf(table));

 Row row = table.getRows().get(2);

 Assert.assertEquals(2, table.indexOf(row));

 Cell cell = row.getLastCell();

 Assert.assertEquals(4, row.indexOf(cell));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Bulunacak düğüm. |

**Returns:**
int - düğüm koleksiyon içinde bulunursa sıfır tabanlı dizin; aksi takdirde -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Belirtilen indekste bir düğümü koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Düğümün sıfır tabanlı dizini. Negatif dizinlere izin verilir ve listedeki sonundan erişimi gösterir. Örneğin -1 son düğümü, -2 sondan bir önceki düğümü ve böyle devam eder. |
| node | [Node](../../com.aspose.words/node/) | Eklenecek düğüm. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar.

**Returns:**
java.util.Iterator - Bir Iterator.
### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Düğümü koleksiyondan ve belgeden kaldırır.

 **Examples:** 

Bir NodeCollection ile nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the document by inserting Runs using a DocumentBuilder.
 builder.write("Run 1. ");
 builder.write("Run 2. ");

 // Every invocation of the "Write()" method creates a new Run,
 // which then appears in the parent Paragraph's RunCollection.
 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertEquals(2, runs.getCount());

 // We can also insert a node into the RunCollection manually.
 Run newRun = new Run(doc, "Run 3. ");
 runs.insert(3, newRun);

 Assert.assertTrue(runs.contains(newRun));
 Assert.assertEquals("Run 1. Run 2. Run 3.", doc.getText().trim());

 // Access individual runs and remove them to remove their text from the document.
 Run run = runs.get(1);
 runs.remove(run);

 Assert.assertEquals("Run 1. Run 3.", doc.getText().trim());
 Assert.assertNotNull(run);
 Assert.assertFalse(runs.contains(run));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Kaldırılacak düğüm. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Belirtilen indeksteki düğümü koleksiyondan ve belgeden kaldırır.

 **Examples:** 

Bir belgede bölümleri nasıl ekleyip kaldıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");

 Assert.assertEquals("Section 1\fSection 2", doc.getText().trim());

 // Delete the first section from the document.
 doc.getSections().removeAt(0);

 Assert.assertEquals("Section 2", doc.getText().trim());

 // Append a copy of what is now the first section to the end of the document.
 int lastSectionIdx = doc.getSections().getCount() - 1;
 Section newSection = doc.getSections().get(lastSectionIdx).deepClone();
 doc.getSections().add(newSection);

 Assert.assertEquals("Section 2\fSection 2", doc.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Düğümün sıfır tabanlı dizini. Negatif dizinlere izin verilir ve listedeki sonundan erişimi gösterir. Örneğin -1 son düğümü, -2 sondan bir önceki düğümü ve böyle devam eder. |

### toArray() {#toArray}
```
public Node[] toArray()
```


Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar.

 **Remarks:** 

Düğümler koleksiyonunu iterasyon sırasında eklememeli/kaldırmamalısınız çünkü bu, yineleyiciyi geçersiz kılar ve canlı koleksiyonlar için yenileme gerektirir.

Iterasyon sırasında düğüm ekleyip/çıkarmak için, bu yöntemi kullanarak düğümleri sabit boyutlu bir diziye kopyalayın ve ardından dizi üzerinde yineleyin.

 **Examples:** 

Tüm metin kutusu şekillerinin nasıl görüntü şekilleriyle değiştirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

**Returns:**
com.aspose.words.Node[] - Düğümlerin bir dizisi.
