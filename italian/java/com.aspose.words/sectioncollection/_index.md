---
title: "SectionCollection"
linktitle: "SectionCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di oggetti Section nel documento in Java."
type: docs
weight: 606
url: /it/java/com.aspose.words/sectioncollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class SectionCollection extends NodeCollection
```

Una raccolta di oggetti [Section](../../com.aspose.words/section/) nel documento.

Per saperne di più, visita l'articolo della documentazione [ Working with Sections ][Working with Sections].

 **Remarks:** 

Un documento Microsoft Word può contenere più sezioni. Per creare una sezione in Microsoft Word, seleziona il comando Inserisci/Interruzione e scegli un tipo di interruzione. L'interruzione specifica se la sezione inizia in una nuova pagina o nella stessa pagina.

L'inserimento e la rimozione programmatica di sezioni può essere usato per personalizzare i documenti prodotti durante la stampa unione. Se un documento deve contenere contenuti diversi o parti di contenuto in base a determinati criteri, è possibile creare un documento \"master\" che contiene più sezioni e cancellare alcune delle sezioni prima o dopo la stampa unione.

 **Examples:** 

Mostra come aggiungere e rimuovere sezioni in un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Aggiunge un nodo alla fine della raccolta. |
| [clear()](#clear) | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Determina se un nodo è nella raccolta. |
| [get(int index)](#get-int) | Recupera una sezione all'indice specificato. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Ottiene il numero di nodi nella raccolta. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Restituisce l'indice basato su zero del nodo specificato. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Inserisce un nodo nella raccolta all'indice specificato. |
| [iterator()](#iterator) | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [remove(Node node)](#remove-com.aspose.words.Node) | Rimuove il nodo dalla raccolta e dal documento. |
| [removeAt(int index)](#removeAt-int) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [toArray()](#toArray) | Copia tutte le sezioni dalla raccolta in un nuovo array di sezioni. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Aggiunge un nodo alla fine della raccolta.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Il nodo da aggiungere alla fine della raccolta. |

### clear() {#clear}
```
public void clear()
```


Rimuove tutti i nodi da questa raccolta e dal documento.

 **Examples:** 

Mostra come rimuovere tutte le sezioni da un documento.

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


Determina se un nodo è nella raccolta.

 **Remarks:** 

Questo metodo esegue una ricerca lineare; pertanto, il tempo medio di esecuzione è proporzionale a [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Mostra come lavorare con una NodeCollection.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Il nodo da individuare. |

**Returns:**
boolean -  true  se l'elemento è trovato nella collezione; altrimenti,  false .
### get(int index) {#get-int}
```
public Node get(int index)
```


Recupera una sezione all'indice specificato.

 **Remarks:** 

L'indice è basato su zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

 **Examples:** 

Mostra quando ricalcolare il layout della pagina del documento.

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

Mostra come preparare un nuovo nodo di sezione per la modifica.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Un indice nella lista delle sezioni. |

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


Ottiene il numero di nodi nella raccolta.

 **Examples:** 

Mostra come attraversare la collezione di nodi figli di un nodo composito.

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

Mostra come verificare se le tabelle sono annidate.

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
int - Il numero di nodi nella collezione.
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Restituisce l'indice basato su zero del nodo specificato.

 **Remarks:** 

Questo metodo esegue una ricerca lineare; pertanto, il tempo medio di esecuzione è proporzionale a [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Mostra come ottenere l'indice di un nodo in una collezione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Il nodo da individuare. |

**Returns:**
int - L'indice basato su zero del nodo nella collezione, se trovato; altrimenti, -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Inserisce un nodo nella raccolta all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero del nodo. Gli indici negativi sono consentiti e indicano l'accesso dalla fine della lista. Per esempio, -1 indica l'ultimo nodo, -2 indica il penultimo e così via. |
| node | [Node](../../com.aspose.words/node/) | Il nodo da inserire. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi.

**Returns:**
java.util.Iterator - Un iteratore.
### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Rimuove il nodo dalla raccolta e dal documento.

 **Examples:** 

Mostra come lavorare con una NodeCollection.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Il nodo da rimuovere. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove il nodo all'indice specificato dalla raccolta e dal documento.

 **Examples:** 

Mostra come aggiungere e rimuovere sezioni in un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice basato su zero del nodo. Gli indici negativi sono consentiti e indicano l'accesso dalla fine della lista. Per esempio, -1 indica l'ultimo nodo, -2 indica il penultimo e così via. |

### toArray() {#toArray}
```
public Node[] toArray()
```


Copia tutte le sezioni dalla raccolta in un nuovo array di sezioni.

**Returns:**
com.aspose.words.Node[] - Un array di sezioni.
