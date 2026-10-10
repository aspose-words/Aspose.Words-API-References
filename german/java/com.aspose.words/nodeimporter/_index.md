---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das effiziente wiederholte Importieren von Knoten von einem Dokument in ein anderes in Java."
type: docs
weight: 480
url: /de/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Ermöglicht das effiziente wiederholte Importieren von Knoten von einem Dokument in ein anderes.

Um mehr zu erfahren, besuchen Sie den [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] Dokumentationsartikel.

 **Remarks:** 

Aspose.Words bietet Funktionalität für einfaches Kopieren und Verschieben von Fragmenten zwischen Microsoft‑Word‑Dokumenten. Dies ist als „Importieren von Knoten“ bekannt. Bevor Sie ein Fragment von einem Dokument in ein anderes einfügen können, müssen Sie es „importieren“. Der Import erstellt einen tiefen Klon des ursprünglichen Knotens, der bereit ist, in das Zieldokument eingefügt zu werden.

Der einfachste Weg, einen Knoten zu importieren, besteht darin, die Methode [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) zu verwenden, die vom Objekt [DocumentBase](../../com.aspose.words/documentbase/) bereitgestellt wird.

Wenn Sie jedoch Knoten mehrfach von einem Dokument in ein anderes importieren müssen, ist es besser, die Klasse [NodeImporter](../../com.aspose.words/nodeimporter/) zu verwenden. Die Klasse [NodeImporter](../../com.aspose.words/nodeimporter/) ermöglicht es, die Anzahl der im Zieldokument erstellten Stile und Listen zu minimieren.

Das Kopieren oder Verschieben von Fragmenten von einem Microsoft‑Word‑Dokument in ein anderes stellt für Aspose.Words eine Reihe technischer Herausforderungen dar. In einem Word‑Dokument werden Stile und Listformatierungen zentral und getrennt vom Text des Dokuments gespeichert. Die Absätze und Textläufe verweisen lediglich über interne eindeutige Kennungen auf die Stile.

Die Herausforderungen ergeben sich daraus, dass Stile und Listen in verschiedenen Dokumenten unterschiedlich sind. Zum Beispiel muss beim Kopieren eines mit dem Stil Überschrift 1 formatierten Absatzes von einem Dokument in ein anderes eine Reihe von Aspekten berücksichtigt werden: entscheiden, ob der Stil Überschrift 1 vom Quell‑ in das Zieldokument kopiert werden soll, den Absatz klonen, den geklonten Absatz aktualisieren, sodass er auf den korrekten Stil Überschrift 1 im Zieldokument verweist. Wenn der Stil kopiert werden muss, sollten alle von ihm referenzierten Stile (basierend auf Stil und nächstem Absatzstil) analysiert und ggf. ebenfalls kopiert werden usw. Ähnliche Probleme treten beim Kopieren von Aufzählungs‑ oder Nummerierungs‑Absätzen auf, da Microsoft Word Listendefinitionen getrennt vom Text speichert.

Die Klasse [NodeImporter](../../com.aspose.words/nodeimporter/) fungiert wie ein Kontext, der während des Imports die „Übersetzungstabellen“ enthält. Sie übersetzt korrekt zwischen Stilen und Listen in Quell‑ und Zieldokumenten.

 **Examples:** 

Zeigt, wie der Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument eingefügt wird.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Initialisiert eine neue Instanz dieser Klasse. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Importiert einen Knoten von einem Dokument in ein anderes. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Importiert einen Knoten von einem Dokument in ein anderes.

 **Remarks:** 

Der Import eines Knotens erstellt eine Kopie des Quellknotens, die zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen übergeordneten Knoten. Der Quellknoten wird weder geändert noch aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss er importiert werden. Beim Import werden dokumentenspezifische Eigenschaften wie Verweise auf Formatvorlagen und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er an die passende Stelle im Dokument eingefügt werden, indem man [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) oder [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) verwendet.

Wenn der Quellknoten bereits zum Ziel‑Dokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

 **Examples:** 

Zeigt, wie der Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument eingefügt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | Der zu importierende Knoten. |
| isImportChildren | boolean | true  zum rekursiven Import aller untergeordneten Knoten; andernfalls  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
