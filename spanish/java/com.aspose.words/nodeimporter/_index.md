---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words para Java"
description: "Permite realizar de manera eficiente importaciones repetidas de nodos de un documento a otro en Java."
type: docs
weight: 480
url: /es/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Permite realizar de forma eficiente la importación repetida de nodos de un documento a otro.

Para obtener más información, visite el artículo de documentación [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Aspose.Words proporciona funcionalidad para copiar y mover fácilmente fragmentos entre documentos de Microsoft Word. Esto se conoce como "importar nodos". Antes de poder insertar un fragmento de un documento en otro, necesita "importarlo". La importación crea un clon profundo del nodo original, listo para ser insertado en el documento de destino.

La forma más sencilla de importar un nodo es usar el método [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) proporcionado por el objeto [DocumentBase](../../com.aspose.words/documentbase/).

Sin embargo, cuando necesita importar nodos de un documento a otro varias veces, es mejor usar la clase [NodeImporter](../../com.aspose.words/nodeimporter/). La clase [NodeImporter](../../com.aspose.words/nodeimporter/) permite minimizar la cantidad de estilos y listas creadas en el documento de destino.

Copiar o mover fragmentos de un documento Microsoft Word a otro presenta una serie de desafíos técnicos para Aspose.Words. En un documento Word, los estilos y el formato de listas se almacenan de forma centralizada, por separado del texto del documento. Los párrafos y las corridas de texto simplemente hacen referencia a los estilos mediante identificadores internos únicos.

Los desafíos surgen del hecho de que los estilos y listas son diferentes en distintos documentos. Por ejemplo, para copiar un párrafo formateado con el estilo Heading 1 de un documento a otro, se deben tener en cuenta varios aspectos: decidir si se copia el estilo Heading 1 del documento origen al documento destino, clonar el párrafo, actualizar el párrafo clonado para que haga referencia al estilo Heading 1 correcto en el documento destino. Si el estilo debe copiarse, todos los estilos que referencia (basados en el estilo y el estilo del siguiente párrafo) deben analizarse y, posiblemente, copiarse también, y así sucesivamente. Problemas similares existen al copiar párrafos con viñetas o numerados porque Microsoft Word almacena las definiciones de listas por separado del texto.

La clase [NodeImporter](../../com.aspose.words/nodeimporter/) es como un contexto que mantiene las \"tablas de traducción\" durante la importación. Traduce correctamente entre estilos y listas en los documentos origen y destino.

 **Examples:** 

Muestra cómo insertar el contenido de un documento en un marcador de otro documento.

```

 public void insertAtBookmark() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("InsertionPoint");
     builder.write("We will insert a document here: ");
     builder.endBookmark("InsertionPoint");

     Document docToInsert = new Document();
     builder = new DocumentBuilder(docToInsert);

     builder.write("Hello world!");

     docToInsert.save(getArtifactsDir() + "NodeImporter.InsertAtMergeField.docx");

     Bookmark bookmark = doc.getRange().getBookmarks().get("InsertionPoint");
     insertDocument(bookmark.getBookmarkStart().getParentNode(), docToInsert);

     Assert.assertEquals("We will insert a document here: " +
             "\rHello world!", doc.getText().trim());
 }

 /// 
 /// Inserts the contents of a document after the specified node.
 /// 
 static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode destinationParent = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         // Loop through all block-level nodes in the section's body,
         // then clone and insert every node that is not the last empty paragraph of a section.
         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 destinationParent.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node should be either a paragraph or table.");
     }
 }
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Inicializa una nueva instancia de esta clase. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Importa un nodo de un documento a otro. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Importa un nodo de un documento a otro.

 **Remarks:** 

Importar un nodo crea una copia del nodo origen que pertenece al documento importador. El nodo devuelto no tiene padre. El nodo origen no se altera ni se elimina del documento original.

Antes de que un nodo de otro documento pueda insertarse en este documento, debe importarse. Durante la importación, las propiedades específicas del documento, como las referencias a estilos y listas, se traducen del original al documento importador. Después de que el nodo se haya importado, puede insertarse en el lugar apropiado del documento usando [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) o [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

Si el nodo origen ya pertenece al documento destino, simplemente se crea un clon profundo del nodo origen.

 **Examples:** 

Muestra cómo insertar el contenido de un documento en un marcador de otro documento.

```

 public void insertAtBookmark() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("InsertionPoint");
     builder.write("We will insert a document here: ");
     builder.endBookmark("InsertionPoint");

     Document docToInsert = new Document();
     builder = new DocumentBuilder(docToInsert);

     builder.write("Hello world!");

     docToInsert.save(getArtifactsDir() + "NodeImporter.InsertAtMergeField.docx");

     Bookmark bookmark = doc.getRange().getBookmarks().get("InsertionPoint");
     insertDocument(bookmark.getBookmarkStart().getParentNode(), docToInsert);

     Assert.assertEquals("We will insert a document here: " +
             "\rHello world!", doc.getText().trim());
 }

 /// 
 /// Inserts the contents of a document after the specified node.
 /// 
 static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode destinationParent = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         // Loop through all block-level nodes in the section's body,
         // then clone and insert every node that is not the last empty paragraph of a section.
         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 destinationParent.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node should be either a paragraph or table.");
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | El nodo a importar. |
| isImportChildren | boolean | true  para importar todos los nodos hijos de forma recursiva; de lo contrario,  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
