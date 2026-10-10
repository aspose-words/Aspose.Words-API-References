---
title: "StructuredDocumentTagRangeStart"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Aspose.Words para Java"
description: "Representa el inicio de una etiqueta de documento estructurado con rango que acepta contenido de múltiples secciones en Java."
type: docs
weight: 640
url: /es/java/com.aspose.words/structureddocumenttagrangestart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/)

**All Implemented Interfaces:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/), java.lang.Iterable
```
public class StructuredDocumentTagRangeStart extends Node implements IStructuredDocumentTag, Iterable
```

Representa el inicio de **ranged** etiqueta de documento estructurado que acepta contenido de múltiples secciones. Consulte también [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/).

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Puede ser hijo inmediato del nodo [Body](../../com.aspose.words/body/) **solo**.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [StructuredDocumentTagRangeStart(DocumentBase doc, int type)](#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Acepta un visitante. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Agrega el nodo especificado al final del rango stdContent. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Crea un duplicado del nodo. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [getAppearance()](#getAppearance) | Obtiene la apariencia de la etiqueta de documento estructurado. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Obtiene el color de la etiqueta de documento estructurado. |
| [getCustomNodeId()](#getCustomNodeId) | Especifica un identificador de nodo personalizado. |
| [getDocument()](#getDocument) | Obtiene el documento al que pertenece este nodo. |
| [getId()](#getId) | Especifica un Id numérico único, de solo lectura y persistente para esta etiqueta de documento estructurado. |
| [getLastChild()](#getLastChild) | Obtiene el último hijo en el rango stdContent. |
| [getLevel()](#getLevel) | Obtiene el nivel en el que ocurre el inicio del rango de esta etiqueta de documento estructurado en el árbol del documento. |
| [getLockContentControl()](#getLockContentControl) | Cuando se establece en true, esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado. |
| [getLockContents()](#getLockContents) | Cuando se establece en true, esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado. |
| [getNextSibling()](#getNextSibling) | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [getNode()](#getNode) |  |
| [getNodeType()](#getNodeType) | Devuelve [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_START](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-START). |
| [getParentNode()](#getParentNode) | Obtiene el padre inmediato de este nodo. |
| [getPlaceholder()](#getPlaceholder) | Obtiene el [BuildingBlock](../../com.aspose.words/buildingblock/) que contiene el texto de marcador de posición que debe mostrarse cuando el contenido de ejecución de esta etiqueta de documento estructurado está vacío, el elemento XML mapeado asociado está vacío según lo especificado mediante el elemento [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart/\#getXmlMapping) o los elementos [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText-boolean) están en true. |
| [getPlaceholderName()](#getPlaceholderName) | Obtiene o establece el Nombre del [BuildingBlock](../../com.aspose.words/buildingblock/) que contiene el texto de marcador de posición. |
| [getPreviousSibling()](#getPreviousSibling) | Obtiene el nodo que precede inmediatamente a este nodo. |
| [getRange()](#getRange) | Devuelve un objeto [Range](../../com.aspose.words/range/) que representa la parte de un documento que está contenida en este nodo. |
| [getRangeEnd()](#getRangeEnd) | Especifica el final del rango si el [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) es una etiqueta de documento estructurado con rango. |
| [getSdtType()](#getSdtType) | Obtiene el tipo de esta etiqueta de documento estructurado. |
| [getTag()](#getTag) | Especifica una etiqueta asociada al nodo actual de la etiqueta de documento estructurado. |
| [getText()](#getText) | Obtiene el texto de este nodo y de todos sus hijos. |
| [getTitle()](#getTitle) | Especifica el nombre descriptivo asociado a esta etiqueta de documento estructurado. |
| [getWordOpenXML()](#getWordOpenXML) | Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC). |
| [getWordOpenXMLMinimal()](#getWordOpenXMLMinimal) | Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC). |
| [getXmlMapping()](#getXmlMapping) | Obtiene un objeto que representa el mapeo de este rango de etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual. |
| [isComposite()](#isComposite) | Devuelve  true  si este nodo puede contener otros nodos. |
| [isMultiSection()](#isMultiSection) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Especifica si el contenido de esta etiqueta de documento estructurado debe interpretarse como texto de marcador de posición (en contraposición al contenido de texto regular dentro de la etiqueta de documento estructurado). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Especifica si el contenido de esta etiqueta de documento estructurado debe interpretarse como texto de marcador de posición (en contraposición al contenido de texto regular dentro de la etiqueta de documento estructurado). |
| [iterator()](#iterator) | Proporciona soporte para la iteración estilo foreach sobre los nodos secundarios de este nodo. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Obtiene el siguiente nodo según el algoritmo de recorrido de árbol en preorden. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Obtiene el nodo anterior según el algoritmo de recorrido de árbol en preorden. |
| [remove()](#remove) | Se elimina a sí mismo del padre. |
| [removeAllChildren()](#removeAllChildren) | Elimina todos los nodos entre este nodo de inicio de rango y el nodo de fin de rango. |
| [removeSelfOnly()](#removeSelfOnly) | Elimina este nodo de inicio de rango y los nodos de fin de rango apropiados de la etiqueta de documento estructurado, pero conserva su contenido dentro del árbol del documento. |
| [setAppearance(int value)](#setAppearance-int) | Establece la apariencia de la etiqueta de documento estructurado. |
| [setColor(Color value)](#setColor-java.awt.Color) | Establece el color de la etiqueta de documento estructurado. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Especifica un identificador de nodo personalizado. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | Cuando se establece en true, esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado. |
| [setLockContents(boolean value)](#setLockContents-boolean) | Cuando se establece en true, esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Obtiene o establece el Nombre del [BuildingBlock](../../com.aspose.words/buildingblock/) que contiene el texto de marcador de posición. |
| [setTag(String value)](#setTag-java.lang.String) | Especifica una etiqueta asociada al nodo actual de la etiqueta de documento estructurado. |
| [setTitle(String value)](#setTitle-java.lang.String) | Especifica el nombre descriptivo asociado a esta etiqueta de documento estructurado. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| [toString(int saveFormat)](#toString-int) |  |
### StructuredDocumentTagRangeStart(DocumentBase doc, int type) {#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int}
```
public StructuredDocumentTagRangeStart(DocumentBase doc, int type)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| tipo | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Acepta un visitante.

 **Remarks:** 

Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en [DocumentVisitor](../../com.aspose.words/documentvisitor/).

Para más información, consulte el patrón de diseño Visitor.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | El visitante que recorrerá los nodos. |

**Returns:**
boolean - Verdadero si se visitaron todos los nodos; falso si [DocumentVisitor](../../com.aspose.words/documentvisitor/) detuvo la operación antes de visitar todos los nodos.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Agrega el nodo especificado al final del rango stdContent.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | El nodo a agregar. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Crea un duplicado del nodo.

 **Remarks:** 

Este método funciona como un constructor de copia para los nodos. El nodo clonado no tiene padre, pero pertenece al mismo documento que el nodo original.

Este método siempre realiza una copia profunda del nodo. El parámetro  isCloneChildren  especifica si también se deben copiar todos los nodos hijos.

 **Examples:** 

Muestra cómo clonar un nodo compuesto.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| isCloneChildren | boolean | Verdadero para clonar recursivamente el subárbol bajo el nodo especificado; falso para clonar solo el nodo en sí. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Obtiene el primer ancestro del tipo de objeto especificado.

 **Remarks:** 

El tipo de ancestro coincide si es igual a  ancestorType  o derivado de  ancestorType .

 **Examples:** 

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ancestorType | java.lang.Class | El tipo de objeto del ancestro a recuperar. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getAppearance() {#getAppearance}
```
public int getAppearance()
```


Obtiene la apariencia de la etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo mostrar la etiqueta alrededor del contenido.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int - La apariencia de la etiqueta de documento estructurado. El valor devuelto es una de las constantes de [SdtAppearance](../../com.aspose.words/sdtappearance/).
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public Color getColor()
```


Obtiene el color de la etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.awt.Color - El color de la etiqueta de documento estructurado.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Especifica un identificador de nodo personalizado.

 **Remarks:** 

El valor predeterminado es cero.

Este identificador puede establecerse y usarse arbitrariamente. Por ejemplo, como una clave para obtener datos externos.

Nota importante, el valor especificado no se guarda en un archivo de salida y solo existe durante la vida del nodo.

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

**Returns:**
int - El valor  int  correspondiente.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Obtiene el documento al que pertenece este nodo.

 **Remarks:** 

El nodo siempre pertenece a un documento, incluso si acaba de ser creado y aún no se ha añadido al árbol, o si ha sido eliminado del árbol.

 **Examples:** 

Muestra cómo crear un nodo y establecer su documento propietario.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getId() {#getId}
```
public int getId()
```


Especifica un Id numérico único, de solo lectura y persistente para esta etiqueta de documento estructurado.

 **Remarks:** 

El atributo Id debe seguir estas reglas:

 *  The document shall retain structured document tag ids only if the whole document is cloned [Document.deepClone()](../../com.aspose.words/document/\#deepClone).
 *  During [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) Id shall be retained if import does not cause conflicts with other structured document tag Ids in the target document.
 *  If multiple structured document tag nodes specify the same decimal number value for the Id attribute, then the first structured document tag in the document shall maintain this original Id, and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
 *  During standalone structured document tag **M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** operation new unique ID will be generated for the cloned structured document tag node.
 *  If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned to it when the document is loaded.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - El valor  int  correspondiente.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Obtiene el último hijo en el rango stdContent.

 **Remarks:** 

Si no hay un nodo hijo último, se devuelve un  null .

**Returns:**
[Node](../../com.aspose.words/node/) - The last child in the stdContent range.
### getLevel() {#getLevel}
```
public int getLevel()
```


Obtiene el nivel en el que ocurre el inicio del rango de esta etiqueta de documento estructurado en el árbol del documento.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - El nivel en el que este inicio de rango de etiqueta de documento estructurado ocurre en el árbol del documento. El valor devuelto es una de las constantes de [MarkupLevel](../../com.aspose.words/markuplevel/).
### getLockContentControl() {#getLockContentControl}
```
public boolean getLockContentControl()
```


Cuando se establece en true, esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getLockContents() {#getLockContents}
```
public boolean getLockContents()
```


Cuando se establece en true, esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Obtiene el nodo que sigue inmediatamente a este nodo.

 **Remarks:** 

Si no hay nodo siguiente, se devuelve un  null  .

 **Examples:** 

Muestra cómo recorrer el árbol de nodos hijos de un nodo compuesto.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

Muestra cómo usar la propiedad NextSibling de un nodo para enumerar sus hijos inmediatos.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNode() {#getNode}
```
public Node getNode()
```


Devuelve un objeto Node que implementa esta interfaz.

**Returns:**
[Node](../../com.aspose.words/node/)
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Devuelve [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_START](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-START).

**Returns:**
int - [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_START](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-START). El valor devuelto es una de las constantes de [NodeType](../../com.aspose.words/nodetype/).
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Obtiene el padre inmediato de este nodo.

 **Remarks:** 

Si un nodo acaba de crearse y aún no se ha añadido al árbol, o si se ha eliminado del árbol, el padre es  null .

 **Examples:** 

Muestra cómo acceder al nodo padre de un nodo.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Muestra cómo crear un nodo y establecer su documento propietario.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPlaceholder() {#getPlaceholder}
```
public BuildingBlock getPlaceholder()
```


Obtiene el [BuildingBlock](../../com.aspose.words/buildingblock/) que contiene el texto de marcador de posición que debe mostrarse cuando el contenido de ejecución de esta etiqueta de documento estructurado está vacío, el elemento XML mapeado asociado está vacío según lo especificado mediante el elemento [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart/\#getXmlMapping) o los elementos [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText-boolean) están en true.

 **Remarks:** 

Puede ser  null , lo que significa que el marcador de posición no es aplicable para esta etiqueta de documento estructurado.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText-boolean) element is  true .
### getPlaceholderName() {#getPlaceholderName}
```
public String getPlaceholderName()
```


Obtiene o establece el Nombre del [BuildingBlock](../../com.aspose.words/buildingblock/) que contiene el texto de marcador de posición.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Obtiene el nodo que precede inmediatamente a este nodo.

 **Remarks:** 

Si no hay nodo precedente, se devuelve un  null  .

 **Examples:** 

Muestra cómo usar los métodos de Node y CompositeNode para eliminar una sección antes de la última sección del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Devuelve un objeto [Range](../../com.aspose.words/range/) que representa la parte de un documento que está contenida en este nodo.

 **Examples:** 

Muestra cómo eliminar todos los nodos de un rango.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRangeEnd() {#getRangeEnd}
```
public StructuredDocumentTagRangeEnd getRangeEnd()
```


Especifica el fin del rango si el [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) es una etiqueta de documento estructurado con rango. De lo contrario, devuelve  null .

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/) - The corresponding [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/) value.
### getSdtType() {#getSdtType}
```
public int getSdtType()
```


Obtiene el tipo de esta etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - Tipo de esta etiqueta de documento estructurado. El valor devuelto es una de las constantes de [SdtType](../../com.aspose.words/sdttype/).
### getTag() {#getTag}
```
public String getTag()
```


Especifica una etiqueta asociada con el nodo de etiqueta de documento estructurado actual. No puede ser  null .

 **Remarks:** 

Una etiqueta es una cadena arbitraria que las aplicaciones pueden asociar con una etiqueta de documento estructurado para identificarla sin proporcionar un nombre amigable visible.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getText() {#getText}
```
public String getText()
```


Obtiene el texto de este nodo y de todos sus hijos.

 **Remarks:** 

La cadena devuelta incluye todos los caracteres de control y especiales según se describe en [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Muestra cómo usar caracteres de control.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert paragraphs with text with DocumentBuilder.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Converting the document to text form reveals that control characters
 // represent some of the document's structural elements, such as page breaks.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         MessageFormat.format("Hello again!{0}", ControlChar.CR) +
         ControlChar.PAGE_BREAK, doc.getText());

 // When converting a document to string form,
 // we can omit some of the control characters with the Trim method.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         "Hello again!", doc.getText().trim());
 
```

Muestra cómo construir un documento Aspose.Words manualmente.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
java.lang.String
### getTitle() {#getTitle}
```
public String getTitle()
```


Especifica el nombre amigable asociado con esta etiqueta de documento estructurado. No puede ser  null .

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getWordOpenXML() {#getWordOpenXML}
```
public String getWordOpenXML()
```


Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.lang.String - Una cadena que representa el XML contenido dentro del nodo en el formato [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).
### getWordOpenXMLMinimal() {#getWordOpenXMLMinimal}
```
public String getWordOpenXMLMinimal()
```


Obtiene una cadena que representa el XML contenido dentro del nodo en el formato [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC). A diferencia de la propiedad [getWordOpenXML()](../../com.aspose.words/structureddocumenttagrangestart/\#getWordOpenXML), este método genera un documento reducido que excluye cualquier parte no relacionada con el contenido.

 **Examples:** 

Muestra cómo obtener el XML mínimo contenido dentro del nodo en el formato FlatOpc.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 Assert.assertTrue(tag.getWordOpenXMLMinimal()
         .contains(
                 ""));
 Assert.assertFalse(tag.getWordOpenXMLMinimal().contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
 
```

**Returns:**
java.lang.String - Una cadena que representa el XML contenido dentro del nodo en el formato [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).
### getXmlMapping() {#getXmlMapping}
```
public XmlMapping getXmlMapping()
```


Obtiene un objeto que representa el mapeo de este rango de etiqueta de documento estructurado a datos XML en una parte XML personalizada del documento actual.

 **Remarks:** 

Puede usar el método [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) de este objeto para mapear un rango de etiqueta de documento estructurado a datos XML.

 **Examples:** 

Muestra cómo establecer mapeos XML para el inicio de rango de una etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart in the document.
 StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 // If we set a mapping for our structured document tag,
 // it will only display a portion of the CustomXmlPart that the XPath points to.
 // This XPath will point to the contents second "" element of the first "" element of our CustomXmlPart.
 sdtRangeStart.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", null);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
 
```

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Devuelve  true  si este nodo puede contener otros nodos. (197141,6)

 **Examples:** 

Muestra cómo recorrer el árbol de nodos hijos de un nodo compuesto.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  si este nodo puede contener otros nodos.
### isMultiSection() {#isMultiSection}
```
public boolean isMultiSection()
```


Devuelve true si esta instancia es una etiqueta de documento estructurado con rango (multi-sección).

 **Examples:** 

Muestra cómo obtener la etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
boolean
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public boolean isShowingPlaceholderText()
```


Especifica si el contenido de esta etiqueta de documento estructurado debe interpretarse como texto de marcador de posición (en contraposición al contenido de texto regular dentro de la etiqueta de documento estructurado).

si se establece en  true , este estado se reanudará (mostrando texto de marcador de posición) al abrir este documento.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public void isShowingPlaceholderText(boolean value)
```


Especifica si el contenido de esta etiqueta de documento estructurado debe interpretarse como texto de marcador de posición (en contraposición al contenido de texto regular dentro de la etiqueta de documento estructurado).

si se establece en  true , este estado se reanudará (mostrando texto de marcador de posición) al abrir este documento.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Proporciona soporte para la iteración estilo foreach sobre los nodos secundarios de este nodo.

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Obtiene el siguiente nodo según el algoritmo de recorrido de árbol en preorden.

 **Examples:** 

Muestra cómo recorrer el árbol de nodos del documento usando el algoritmo de recorrido preorden, y eliminar cualquier forma encontrada con una imagen.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | El nodo superior (límite) del recorrido. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Obtiene el nodo anterior según el algoritmo de recorrido de árbol en preorden.

 **Examples:** 

Muestra cómo recorrer el árbol de nodos del documento usando el algoritmo de recorrido preorden, y eliminar cualquier forma encontrada con una imagen.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | El nodo superior (límite) del recorrido. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Se elimina a sí mismo del padre.

 **Examples:** 

Muestra cómo eliminar todas las formas con imágenes de un documento.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

Muestra cómo eliminar todos los nodos hijos de un tipo específico de un nodo compuesto.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Elimina todos los nodos entre este nodo de inicio de rango y el nodo de fin de rango.

 **Examples:** 

Muestra cómo crear/eliminar una etiqueta de documento estructurado y su contenido.

```
{@code
 public void sdtRangeExtendedMethods() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("StructuredDocumentTag element");

     StructuredDocumentTagRangeStart rangeStart = insertStructuredDocumentTagRanges(doc);

     // Removes ranged structured document tag, but keeps content inside.
     rangeStart.removeSelfOnly();

     rangeStart = (StructuredDocumentTagRangeStart)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, false);
     Assert.assertEquals(null, rangeStart);

     StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, 0, false);

     Assert.assertEquals(null, rangeEnd);
     Assert.assertEquals("StructuredDocumentTag element", doc.getText().trim());

     rangeStart = insertStructuredDocumentTagRanges(doc);

     Node paragraphNode = rangeStart.getLastChild();
     if (paragraphNode != null)
         Assert.assertEquals("StructuredDocumentTag element", paragraphNode.getText().trim());

     // Removes ranged structured document tag and content inside.
     rangeStart.removeAllChildren();

     paragraphNode = rangeStart.getLastChild();
     Assert.assertEquals("",  paragraphNode.getText());
 }
```

### removeSelfOnly() {#removeSelfOnly}
```
public void removeSelfOnly()
```


Elimina este nodo de inicio de rango y los nodos de fin de rango apropiados de la etiqueta de documento estructurado, pero conserva su contenido dentro del árbol del documento.

 **Examples:** 

Muestra cómo crear/eliminar una etiqueta de documento estructurado y su contenido.

```
{@code
 public void sdtRangeExtendedMethods() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("StructuredDocumentTag element");

     StructuredDocumentTagRangeStart rangeStart = insertStructuredDocumentTagRanges(doc);

     // Removes ranged structured document tag, but keeps content inside.
     rangeStart.removeSelfOnly();

     rangeStart = (StructuredDocumentTagRangeStart)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, false);
     Assert.assertEquals(null, rangeStart);

     StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, 0, false);

     Assert.assertEquals(null, rangeEnd);
     Assert.assertEquals("StructuredDocumentTag element", doc.getText().trim());

     rangeStart = insertStructuredDocumentTagRanges(doc);

     Node paragraphNode = rangeStart.getLastChild();
     if (paragraphNode != null)
         Assert.assertEquals("StructuredDocumentTag element", paragraphNode.getText().trim());

     // Removes ranged structured document tag and content inside.
     rangeStart.removeAllChildren();

     paragraphNode = rangeStart.getLastChild();
     Assert.assertEquals("",  paragraphNode.getText());
 }
```

### setAppearance(int value) {#setAppearance-int}
```
public void setAppearance(int value)
```


Establece la apariencia de la etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo mostrar la etiqueta alrededor del contenido.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | La apariencia de la etiqueta de documento estructurado. El valor debe ser uno de los constantes de [SdtAppearance](../../com.aspose.words/sdtappearance/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Establece el color de la etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color de la etiqueta de documento estructurado. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Especifica un identificador de nodo personalizado.

 **Remarks:** 

El valor predeterminado es cero.

Este identificador puede establecerse y usarse arbitrariamente. Por ejemplo, como una clave para obtener datos externos.

Nota importante, el valor especificado no se guarda en un archivo de salida y solo existe durante la vida del nodo.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public void setLockContentControl(boolean value)
```


Cuando se establece en true, esta propiedad prohibirá que un usuario elimine esta etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public void setLockContents(boolean value)
```


Cuando se establece en true, esta propiedad prohibirá que un usuario edite el contenido de esta etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public void setPlaceholderName(String value)
```


Obtiene o establece el Nombre del [BuildingBlock](../../com.aspose.words/buildingblock/) que contiene el texto de marcador de posición.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setTag(String value) {#setTag-java.lang.String}
```
public void setTag(String value)
```


Especifica una etiqueta asociada con el nodo de etiqueta de documento estructurado actual. No puede ser  null .

 **Remarks:** 

Una etiqueta es una cadena arbitraria que las aplicaciones pueden asociar con una etiqueta de documento estructurado para identificarla sin proporcionar un nombre amigable visible.

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Especifica el nombre amigable asociado con esta etiqueta de documento estructurado. No puede ser  null .

 **Examples:** 

Muestra cómo obtener las propiedades de las etiquetas de documento estructurado multi-sección.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas.

 **Examples:** 

Exporta el contenido de un nodo a String en formato HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Especifica las opciones que controlan cómo se guarda el nodo. |

**Returns:**
java.lang.String - El contenido del nodo en el formato especificado.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
