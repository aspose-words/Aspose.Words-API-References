---
title: "SectionCollection"
linktitle: "SectionCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de objetos Section en el documento en Java."
type: docs
weight: 606
url: /es/java/com.aspose.words/sectioncollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class SectionCollection extends NodeCollection
```

Una colección de objetos [Section](../../com.aspose.words/section/) en el documento.

Para obtener más información, visite el artículo de documentación [ Working with Sections ][Working with Sections].

 **Remarks:** 

Un documento de Microsoft Word puede contener múltiples secciones. Para crear una sección en Microsoft Word, seleccione el comando Insertar/Salto y elija un tipo de salto. El salto especifica si la sección comienza en una página nueva o en la misma página.

Insertar y eliminar secciones programáticamente puede usarse para personalizar documentos generados durante la combinación de correspondencia. Si un documento necesita tener contenido diferente o partes del contenido según ciertos criterios, puede crear un documento \"master\" que contenga múltiples secciones y eliminar algunas de las secciones antes o después de la combinación de correspondencia.

 **Examples:** 

Muestra cómo agregar y eliminar secciones en un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Agrega un nodo al final de la colección. |
| [clear()](#clear) | Elimina todos los nodos de esta colección y del documento. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Determina si un nodo está en la colección. |
| [get(int index)](#get-int) | Recupera una sección en el índice dado. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Obtiene el número de nodos en la colección. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Devuelve el índice basado en cero del nodo especificado. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Inserta un nodo en la colección en el índice especificado. |
| [iterator()](#iterator) | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [remove(Node node)](#remove-com.aspose.words.Node) | Elimina el nodo de la colección y del documento. |
| [removeAt(int index)](#removeAt-int) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [toArray()](#toArray) | Copia todas las secciones de la colección a una nueva matriz de secciones. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Agrega un nodo al final de la colección.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | El nodo que se agregará al final de la colección. |

### clear() {#clear}
```
public void clear()
```


Elimina todos los nodos de esta colección y del documento.

 **Examples:** 

Muestra cómo eliminar todas las secciones de un documento.

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


Determina si un nodo está en la colección.

 **Remarks:** 

Este método realiza una búsqueda lineal; por lo tanto, el tiempo de ejecución promedio es proporcional a [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Muestra cómo trabajar con un NodeCollection.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | El nodo a localizar. |

**Returns:**
boolean -  true  si el elemento se encuentra en la colección; de lo contrario,  false .
### get(int index) {#get-int}
```
public Node get(int index)
```


Recupera una sección en el índice dado.

 **Remarks:** 

El índice comienza en cero.

Se permiten índices negativos e indican acceso desde el final de la colección. Por ejemplo, -1 significa el último elemento, -2 significa el penúltimo y así sucesivamente.

Si el índice es mayor o igual que el número de elementos en la lista, esto devuelve una referencia nula.

Si el índice es negativo y su valor absoluto es mayor que el número de elementos en la lista, esto devuelve una referencia nula.

 **Examples:** 

Muestra cuándo recalcular el diseño de página del documento.

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

Muestra cómo preparar un nuevo nodo de sección para su edición.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Un índice en la lista de secciones. |

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


Obtiene el número de nodos en la colección.

 **Examples:** 

Muestra cómo recorrer la colección de nodos hijos de un nodo compuesto.

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

Muestra cómo averiguar si una tabla está anidada.

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
int - El número de nodos en la colección.
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Devuelve el índice basado en cero del nodo especificado.

 **Remarks:** 

Este método realiza una búsqueda lineal; por lo tanto, el tiempo de ejecución promedio es proporcional a [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Muestra cómo obtener el índice de un nodo en una colección.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | El nodo a localizar. |

**Returns:**
int - El índice basado en cero del nodo dentro de la colección, si se encuentra; de lo contrario, -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Inserta un nodo en la colección en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero del nodo. Se permiten índices negativos e indican acceso desde el final de la lista. Por ejemplo, -1 significa el último nodo, -2 significa el penúltimo y así sucesivamente. |
| node | [Node](../../com.aspose.words/node/) | El nodo a insertar. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos.

**Returns:**
java.util.Iterator - Un iterador.
### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Elimina el nodo de la colección y del documento.

 **Examples:** 

Muestra cómo trabajar con un NodeCollection.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | El nodo a eliminar. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina el nodo en el índice especificado de la colección y del documento.

 **Examples:** 

Muestra cómo agregar y eliminar secciones en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero del nodo. Se permiten índices negativos e indican acceso desde el final de la lista. Por ejemplo, -1 significa el último nodo, -2 significa el penúltimo y así sucesivamente. |

### toArray() {#toArray}
```
public Node[] toArray()
```


Copia todas las secciones de la colección a una nueva matriz de secciones.

**Returns:**
com.aspose.words.Node[] - Una matriz de secciones.
