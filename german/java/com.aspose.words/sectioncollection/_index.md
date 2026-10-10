---
title: "SectionCollection"
linktitle: "SectionCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von Section‑Objekten im Dokument in Java."
type: docs
weight: 606
url: /de/java/com.aspose.words/sectioncollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class SectionCollection extends NodeCollection
```

Eine Sammlung von [Section](../../com.aspose.words/section/)‑Objekten im Dokument.

Um mehr zu erfahren, besuchen Sie den [ Working with Sections ][Working with Sections] Dokumentationsartikel.

 **Remarks:** 

Ein Microsoft‑Word‑Dokument kann mehrere Abschnitte enthalten. Um einen Abschnitt in Microsoft Word zu erstellen, wählen Sie den Befehl Einfügen/Umbruch und wählen Sie einen Umbruchtyp aus. Der Umbruch legt fest, ob der Abschnitt auf einer neuen Seite oder auf derselben Seite beginnt.

Das programmgesteuerte Einfügen und Entfernen von Abschnitten kann verwendet werden, um Dokumente, die beim Seriendruck erstellt werden, anzupassen. Wenn ein Dokument je nach Kriterien unterschiedliche Inhalte oder Teile davon enthalten muss, können Sie ein "master"-Dokument erstellen, das mehrere Abschnitte enthält, und einige der Abschnitte vor oder nach dem Seriendruck löschen.

 **Examples:** 

Zeigt, wie man Abschnitte in einem Dokument hinzufügt und entfernt.

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


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [clear()](#clear) | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get(int index)](#get-int) | Ruft einen Abschnitt am angegebenen Index ab. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Fügt einen Knoten an dem angegebenen Index in die Sammlung ein. |
| [iterator()](#iterator) | Stellt eine einfache \"foreach\"‑artige Iteration über die Sammlung von Knoten bereit. |
| [remove(Node node)](#remove-com.aspose.words.Node) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [removeAt(int index)](#removeAt-int) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [toArray()](#toArray) | Kopiert alle Abschnitte aus der Sammlung in ein neues Array von Abschnitten. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Fügt einen Knoten am Ende der Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Der Knoten, der am Ende der Sammlung hinzugefügt werden soll. |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument.

 **Examples:** 

Zeigt, wie alle Abschnitte aus einem Dokument entfernt werden.

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


Bestimmt, ob ein Knoten in der Sammlung ist.

 **Remarks:** 

Diese Methode führt eine lineare Suche durch; daher ist die durchschnittliche Ausführungszeit proportional zu [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Zeigt, wie man mit einer NodeCollection arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Der zu lokalisierende Knoten. |

**Returns:**
boolean - true, wenn das Element in der Sammlung gefunden wird; andernfalls false.
### get(int index) {#get-int}
```
public Node get(int index)
```


Ruft einen Abschnitt am angegebenen Index ab.

 **Remarks:** 

Der Index ist nullbasiert.

Negative Indizes sind zulässig und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

 **Examples:** 

Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden soll.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

Zeigt, wie ein neuer Abschnittsknoten zur Bearbeitung vorbereitet wird.

```

 Document doc = new Document();

 // A blank document comes with a section, which has a body, which in turn has a paragraph.
 // We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
 Assert.assertEquals(NodeType.SECTION, doc.getChild(NodeType.ANY, 0, true).getNodeType());
 Assert.assertEquals(NodeType.BODY, doc.getSections().get(0).getChild(NodeType.ANY, 0, true).getNodeType());
 Assert.assertEquals(NodeType.PARAGRAPH, doc.getSections().get(0).getBody().getChild(NodeType.ANY, 0, true).getNodeType());

 // If we add a new section like this, it will not have a body, or any other child nodes.
 doc.getSections().add(new Section(doc));

 Assert.assertEquals(0, doc.getSections().get(1).getChildNodes(NodeType.ANY, true).getCount());

 // Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
 doc.getLastSection().ensureMinimum();

 Assert.assertEquals(NodeType.BODY, doc.getSections().get(1).getChild(NodeType.ANY, 0, true).getNodeType());
 Assert.assertEquals(NodeType.PARAGRAPH, doc.getSections().get(1).getBody().getChild(NodeType.ANY, 0, true).getNodeType());

 doc.getSections().get(0).getBody().getFirstParagraph().appendChild(new Run(doc, "Hello world!"));

 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Liste der Abschnitte. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [Section](../../com.aspose.words/section/) value.
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


Ermittelt die Anzahl der Knoten in der Sammlung.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

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

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

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
int - Die Anzahl der Knoten in der Sammlung.
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Gibt den nullbasierten Index des angegebenen Knotens zurück.

 **Remarks:** 

Diese Methode führt eine lineare Suche durch; daher ist die durchschnittliche Ausführungszeit proportional zu [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Zeigt, wie man den Index eines Knotens in einer Sammlung erhält.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Der zu lokalisierende Knoten. |

**Returns:**
int - Der nullbasierte Index des Knotens innerhalb der Sammlung, falls gefunden; andernfalls -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Fügt einen Knoten an dem angegebenen Index in die Sammlung ein.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index des Knotens. Negative Indizes sind zulässig und bedeuten Zugriff vom Ende der Liste. Zum Beispiel bedeutet -1 den letzten Knoten, -2 den vorletzten und so weiter. |
| node | [Node](../../com.aspose.words/node/) | Der einzufügende Knoten. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Stellt eine einfache \"foreach\"‑artige Iteration über die Sammlung von Knoten bereit.

**Returns:**
java.util.Iterator - Ein Iterator.
### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Entfernt den Knoten aus der Sammlung und aus dem Dokument.

 **Examples:** 

Zeigt, wie man mit einer NodeCollection arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Der zu entfernende Knoten. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument.

 **Examples:** 

Zeigt, wie man Abschnitte in einem Dokument hinzufügt und entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index des Knotens. Negative Indizes sind zulässig und bedeuten Zugriff vom Ende der Liste. Zum Beispiel bedeutet -1 den letzten Knoten, -2 den vorletzten und so weiter. |

### toArray() {#toArray}
```
public Node[] toArray()
```


Kopiert alle Abschnitte aus der Sammlung in ein neues Array von Abschnitten.

**Returns:**
com.aspose.words.Node[] – Ein Array von Abschnitten.
