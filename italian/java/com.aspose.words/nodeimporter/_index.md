---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words per Java"
description: "Consente di eseguire in modo efficiente importazioni ripetute di nodi da un documento all'altro in Java."
type: docs
weight: 480
url: /it/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Consente di eseguire in modo efficiente l'importazione ripetuta di nodi da un documento a un altro.

Per saperne di più, visita l'articolo della documentazione [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Aspose.Words fornisce funzionalità per copiare e spostare facilmente frammenti tra documenti Microsoft Word. Questo è noto come "importazione di nodi". Prima di poter inserire un frammento da un documento a un altro, è necessario "importarlo". L'importazione crea un clone profondo del nodo originale, pronto per essere inserito nel documento di destinazione.

Il modo più semplice per importare un nodo è utilizzare il metodo [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/#importNode-com.aspose.words.Node--boolean) fornito dall'oggetto [DocumentBase](../../com.aspose.words/documentbase/).

Tuttavia, quando è necessario importare nodi da un documento a un altro più volte, è preferibile utilizzare la classe [NodeImporter](../../com.aspose.words/nodeimporter/). La classe [NodeImporter](../../com.aspose.words/nodeimporter/) consente di ridurre al minimo il numero di stili e di elenchi creati nel documento di destinazione.

Copiare o spostare frammenti da un documento Microsoft Word a un altro presenta una serie di sfide tecniche per Aspose.Words. In un documento Word, gli stili e la formattazione delle liste sono memorizzati centralmente, separatamente dal testo del documento. I paragrafi e le sequenze di testo fanno semplicemente riferimento agli stili tramite identificatori unici interni.

Le sfide derivano dal fatto che gli stili e le liste sono diversi nei vari documenti. Ad esempio, per copiare un paragrafo formattato con lo stile Heading 1 da un documento a un altro, è necessario considerare diversi aspetti: decidere se copiare lo stile Heading 1 dal documento di origine al documento di destinazione, clonare il paragrafo, aggiornare il paragrafo clonato in modo che faccia riferimento allo stile Heading 1 corretto nel documento di destinazione. Se lo stile deve essere copiato, tutti gli stili a cui fa riferimento (basati sullo stile e sullo stile del paragrafo successivo) dovrebbero essere analizzati e possibilmente copiati anch'essi, e così via. Problemi simili si verificano quando si copiano paragrafi puntati o numerati perché Microsoft Word memorizza le definizioni delle liste separatamente dal testo.

La classe [NodeImporter](../../com.aspose.words/nodeimporter/) è simile a un contesto, che contiene le "tabelle di traduzione" durante l'importazione. Traduce correttamente tra stili e liste nei documenti di origine e di destinazione.

 **Examples:** 

Mostra come inserire il contenuto di un documento in un segnalibro di un altro documento.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Inizializza una nuova istanza di questa classe. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Importa un nodo da un documento a un altro. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Importa un nodo da un documento a un altro.

 **Remarks:** 

L'importazione di un nodo crea una copia del nodo di origine appartenente al documento di importazione. Il nodo restituito non ha genitore. Il nodo di origine non viene modificato né rimosso dal documento originale.

Prima che un nodo proveniente da un altro documento possa essere inserito in questo documento, deve essere importato. Durante l'importazione, le proprietà specifiche del documento, come i riferimenti a stili e liste, vengono tradotte dall'originale al documento di importazione. Dopo che il nodo è stato importato, può essere inserito nel punto appropriato del documento usando [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) o [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

Se il nodo di origine appartiene già al documento di destinazione, viene semplicemente creata una clonazione profonda del nodo di origine.

 **Examples:** 

Mostra come inserire il contenuto di un documento in un segnalibro di un altro documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | Il nodo da importare. |
| isImportChildren | boolean | true  per importare tutti i nodi figlio ricorsivamente; altrimenti,  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
