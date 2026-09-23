---
title: "HeaderFooterCollection"
linktitle: "HeaderFooterCollection"
second_title: "Aspose.Words pour Java"
description: "Fournit un accès typé aux nœuds HeaderFooter d’une Section en Java."
type: docs
weight: 371
url: /fr/java/com.aspose.words/headerfootercollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class HeaderFooterCollection extends NodeCollection
```

Fournit un accès typé aux nœuds [HeaderFooter](../../com.aspose.words/headerfooter/) d’une [Section](../../com.aspose.words/section/).

Pour en savoir plus, consultez l’article de documentation [ Working with Headers and Footers ][Working with Headers and Footers].

 **Remarks:** 

Il ne peut y avoir au maximum qu’un [HeaderFooter](../../com.aspose.words/headerfooter/)

de chaque [HeaderFooterType](../../com.aspose.words/headerfootertype/) par [Section](../../com.aspose.words/section/).

[HeaderFooter](../../com.aspose.words/headerfooter/) objects can occur in any order in the collection.

 **Examples:** 

Montre comment créer un en-tête et un pied de page.

```

 Document doc = new Document();

 // Create a header and append a paragraph to it. The text in that paragraph
 // will appear at the top of every page of this section, above the main body text.
 HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(header);

 Paragraph para = header.appendParagraph("My header.");

 Assert.assertTrue(header.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 // Create a footer and append a paragraph to it. The text in that paragraph
 // will appear at the bottom of every page of this section, below the main body text.
 HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(footer);

 para = footer.appendParagraph("My footer.");

 Assert.assertFalse(footer.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 Assert.assertEquals(para.getParentStory(), footer);
 Assert.assertEquals(para.getParentSection(), footer.getParentSection());
 Assert.assertEquals(header.getParentSection(), footer.getParentSection());

 doc.save(getArtifactsDir() + "HeaderFooter.Create.docx");
 
```

Montre comment supprimer tous les pieds de page d'un document.

```

 Document doc = new Document(getMyDir() + "Header and footer types.docx");

 // Iterate through each section and remove footers of every kind.
 for (Section section : doc.getSections()) {
     // There are three kinds of footer and header types.
     // 1 -  The "First" header/footer, which only appears on the first page of a section.
     HeaderFooter footer = section.getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_FIRST);
     if (footer != null) {
         footer.remove();
     }

     // 2 -  The "Primary" header/footer, which appears on odd pages.
     footer = section.getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);
     if (footer != null) {
         footer.remove();
     }

     // 3 -  The "Even" header/footer, which appears on even pages.
     footer = section.getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_EVEN);
     if (footer != null) {
         footer.remove();
     }

     Assert.assertEquals(0, IterableUtils.countMatches(section.getHeadersFooters(), s -> !s.isHeader()));
 }

 doc.save(getArtifactsDir() + "HeaderFooter.RemoveFooters.docx");
 
```


[Working with Headers and Footers]: https://docs.aspose.com/words/java/working-with-headers-and-footers/
## Méthodes

| Méthode | Description |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Ajoute un nœud à la fin de la collection. |
| [clear()](#clear) | Supprime tous les nœuds de cette collection et du document. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Détermine si un nœud se trouve dans la collection. |
| [get(int index)](#get-int) | Récupère un [HeaderFooter](../../com.aspose.words/headerfooter/) à l'index donné. |
| [getByHeaderFooterType(int headerFooterType)](#getByHeaderFooterType-int) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Obtient le nombre de nœuds dans la collection. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Insère un nœud dans la collection à l'index spécifié. |
| [iterator()](#iterator) | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [linkToPrevious(boolean isLinkToPrevious)](#linkToPrevious-boolean) | Lie ou délie tous les en-têtes et pieds de page aux en-têtes et pieds de page correspondants de la section précédente. |
| [linkToPrevious(int headerFooterType, boolean isLinkToPrevious)](#linkToPrevious-int-boolean) |  |
| [remove(Node node)](#remove-com.aspose.words.Node) | Supprime le nœud de la collection et du document. |
| [removeAt(int index)](#removeAt-int) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [toArray()](#toArray) | Copie tous les  HeaderFooter  s de la collection vers un nouveau tableau de  HeaderFooter  s. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Ajoute un nœud à la fin de la collection.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Le nœud à ajouter à la fin de la collection. |

### clear() {#clear}
```
public void clear()
```


Supprime tous les nœuds de cette collection et du document.

 **Examples:** 

Montre comment supprimer toutes les sections d'un document.

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


Détermine si un nœud se trouve dans la collection.

 **Remarks:** 

Cette méthode effectue une recherche linéaire ; par conséquent, le temps d'exécution moyen est proportionnel à [getCount()](../../com.aspose.words/nodecollection/\\#getCount).

 **Examples:** 

Montre comment travailler avec un NodeCollection.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Le nœud à localiser. |

**Returns:**
booléen -  true  si l'élément est trouvé dans la collection ; sinon,  false .
### get(int index) {#get-int}
```
public Node get(int index)
```


Récupère un [HeaderFooter](../../com.aspose.words/headerfooter/) à l'index donné.

 **Remarks:** 

L'index est basé sur zéro.

Les index négatifs sont autorisés et indiquent un accès depuis la fin de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

 **Examples:** 

Montre comment lier les en-têtes et pieds de page entre les sections.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 3");

 // Move to the first section and create a header and a footer. By default,
 // the header and the footer will only appear on pages in the section that contains them.
 builder.moveToSection(0);

 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header, which will be displayed in sections 1 and 2.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer, which will be displayed in sections 1, 2 and 3.");

 // We can link a section's headers/footers to the previous section's headers/footers
 // to allow the linking section to display the linked section's headers/footers.
 doc.getSections().get(1).getHeadersFooters().linkToPrevious(true);

 // Each section will still have its own header/footer objects. When we link sections,
 // the linking section will display the linked section's header/footers while keeping its own.
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0), doc.getSections().get(1).getHeadersFooters().get(0));
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0).getParentSection(), doc.getSections().get(1).getHeadersFooters().get(0).getParentSection());

 // Link the headers/footers of the third section to the headers/footers of the second section.
 // The second section already links to the first section's header/footers,
 // so linking to the second section will create a link chain.
 // The first, second, and now the third sections will all display the first section's headers.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(true);

 // We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(false);

 // We can also select only a specific type of header/footer to link using this method.
 // The third section now will have the same footer as the second and first sections, but not the header.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(HeaderFooterType.FOOTER_PRIMARY, true);

 // The first section's header/footers cannot link themselves to anything because there is no previous section.
 Assert.assertEquals(2, doc.getSections().get(0).getHeadersFooters().getCount());
 Assert.assertEquals(0, IterableUtils.countMatches(doc.getSections().get(0).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // All the second section's header/footers are linked to the first section's headers/footers.
 Assert.assertEquals(6, doc.getSections().get(1).getHeadersFooters().getCount());
 Assert.assertEquals(6, IterableUtils.countMatches(doc.getSections().get(1).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // In the third section, only the footer is linked to the first section's footer via the second section.
 Assert.assertEquals(6, doc.getSections().get(2).getHeadersFooters().getCount());
 Assert.assertEquals(1, IterableUtils.countMatches(doc.getSections().get(2).getHeadersFooters(), s -> s.isLinkedToPrevious()));
 Assert.assertTrue(doc.getSections().get(2).getHeadersFooters().get(3).isLinkedToPrevious());

 doc.save(getArtifactsDir() + "HeaderFooter.Link.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [HeaderFooter](../../com.aspose.words/headerfooter/) value.
### getByHeaderFooterType(int headerFooterType) {#getByHeaderFooterType-int}
```
public HeaderFooter getByHeaderFooterType(int headerFooterType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
[HeaderFooter](../../com.aspose.words/headerfooter/)
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


Obtient le nombre de nœuds dans la collection.

 **Examples:** 

Montre comment parcourir la collection de nœuds enfants d'un nœud composite.

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

Montre comment déterminer si des tables sont imbriquées.

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
int - Le nombre de nœuds dans la collection.
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
| Paramètre | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Renvoie l'index basé sur zéro du nœud spécifié.

 **Remarks:** 

Cette méthode effectue une recherche linéaire ; par conséquent, le temps d'exécution moyen est proportionnel à [getCount()](../../com.aspose.words/nodecollection/\\#getCount).

 **Examples:** 

Montre comment obtenir l'index d'un nœud dans une collection.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Le nœud à localiser. |

**Returns:**
int - L'index basé sur zéro du nœud dans la collection, s'il est trouvé ; sinon, -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Insère un nœud dans la collection à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro du nœud. Les index négatifs sont autorisés et indiquent un accès depuis la fin de la liste. Par exemple, -1 signifie le dernier nœud, -2 signifie l'avant-dernier et ainsi de suite. |
| node | [Node](../../com.aspose.words/node/) | Le nœud à insérer. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Fournit une itération simple de type "foreach" sur la collection de nœuds.

**Returns:**
java.util.Iterator - Un itérateur.
### linkToPrevious(boolean isLinkToPrevious) {#linkToPrevious-boolean}
```
public void linkToPrevious(boolean isLinkToPrevious)
```


Lie ou délie tous les en-têtes et pieds de page aux en-têtes et pieds de page correspondants de la section précédente.

 **Remarks:** 

Si l'un des en-têtes ou pieds de page n'existe pas, les crée automatiquement.

 **Examples:** 

Montre comment lier les en-têtes et pieds de page entre les sections.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 3");

 // Move to the first section and create a header and a footer. By default,
 // the header and the footer will only appear on pages in the section that contains them.
 builder.moveToSection(0);

 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header, which will be displayed in sections 1 and 2.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer, which will be displayed in sections 1, 2 and 3.");

 // We can link a section's headers/footers to the previous section's headers/footers
 // to allow the linking section to display the linked section's headers/footers.
 doc.getSections().get(1).getHeadersFooters().linkToPrevious(true);

 // Each section will still have its own header/footer objects. When we link sections,
 // the linking section will display the linked section's header/footers while keeping its own.
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0), doc.getSections().get(1).getHeadersFooters().get(0));
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0).getParentSection(), doc.getSections().get(1).getHeadersFooters().get(0).getParentSection());

 // Link the headers/footers of the third section to the headers/footers of the second section.
 // The second section already links to the first section's header/footers,
 // so linking to the second section will create a link chain.
 // The first, second, and now the third sections will all display the first section's headers.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(true);

 // We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(false);

 // We can also select only a specific type of header/footer to link using this method.
 // The third section now will have the same footer as the second and first sections, but not the header.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(HeaderFooterType.FOOTER_PRIMARY, true);

 // The first section's header/footers cannot link themselves to anything because there is no previous section.
 Assert.assertEquals(2, doc.getSections().get(0).getHeadersFooters().getCount());
 Assert.assertEquals(0, IterableUtils.countMatches(doc.getSections().get(0).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // All the second section's header/footers are linked to the first section's headers/footers.
 Assert.assertEquals(6, doc.getSections().get(1).getHeadersFooters().getCount());
 Assert.assertEquals(6, IterableUtils.countMatches(doc.getSections().get(1).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // In the third section, only the footer is linked to the first section's footer via the second section.
 Assert.assertEquals(6, doc.getSections().get(2).getHeadersFooters().getCount());
 Assert.assertEquals(1, IterableUtils.countMatches(doc.getSections().get(2).getHeadersFooters(), s -> s.isLinkedToPrevious()));
 Assert.assertTrue(doc.getSections().get(2).getHeadersFooters().get(3).isLinkedToPrevious());

 doc.save(getArtifactsDir() + "HeaderFooter.Link.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | boolean | true  pour lier les en-têtes et pieds de page à la section précédente ;  false  pour les délier. |

### linkToPrevious(int headerFooterType, boolean isLinkToPrevious) {#linkToPrevious-int-boolean}
```
public void linkToPrevious(int headerFooterType, boolean isLinkToPrevious)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |
| isLinkToPrevious | boolean |  |

### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Supprime le nœud de la collection et du document.

 **Examples:** 

Montre comment travailler avec un NodeCollection.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Le nœud à supprimer. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime le nœud à l'index spécifié de la collection et du document.

 **Examples:** 

Montre comment ajouter et supprimer des sections dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index basé sur zéro du nœud. Les index négatifs sont autorisés et indiquent un accès depuis la fin de la liste. Par exemple, -1 signifie le dernier nœud, -2 signifie l'avant-dernier et ainsi de suite. |

### toArray() {#toArray}
```
public HeaderFooter[] toArray()
```


Copie tous les  HeaderFooter  s de la collection vers un nouveau tableau de  HeaderFooter  s.

 **Examples:** 

Montre comment imprimer la structure des nœuds de chaque en-tête et pied de page dans un document.

```

 public void headerFooterToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());

     // An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
     HeaderFooter[] headerFooters = doc.getFirstSection().getHeadersFooters().toArray();
     Assert.assertEquals(3, headerFooters.length);
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered HeaderFooter nodes and their children.
 /// 
 public static class HeaderFooterStructurePrinter extends DocumentVisitor {
     public HeaderFooterStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideHeaderFooter = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideHeaderFooter) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a HeaderFooter node is encountered in the document.
     /// 
     public int visitHeaderFooterStart(final HeaderFooter headerFooter) {
         indentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.getHeaderFooterType());
         mDocTraversalDepth++;
         mVisitorIsInsideHeaderFooter = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a HeaderFooter node have been visited.
     /// 
     public int visitHeaderFooterEnd(final HeaderFooter headerFooter) {
         mDocTraversalDepth--;
         indentAndAppendLine("[HeaderFooter end]");
         mVisitorIsInsideHeaderFooter = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideHeaderFooter;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
com.aspose.words.HeaderFooter[] - Un tableau de  HeaderFooter  s.
