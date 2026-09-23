---
title: "NodeImporter"
linktitle: "NodeImporter"
second_title: "Aspose.Words pour Java"
description: "Permet d'effectuer efficacement des importations répétées de nœuds d'un document à un autre en Java."
type: docs
weight: 480
url: /fr/java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Permet d'effectuer efficacement des importations répétées de nœuds d'un document à un autre.

Pour en savoir plus, consultez l'article de documentation [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_].

 **Remarks:** 

Aspose.Words offre des fonctionnalités pour copier et déplacer facilement des fragments entre des documents Microsoft Word. Cela s'appelle "importation de nœuds". Avant de pouvoir insérer un fragment d'un document dans un autre, vous devez l"importer". L'importation crée un clone profond du nœud original, prêt à être inséré dans le document de destination.

La façon la plus simple d'importer un nœud est d'utiliser la méthode [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) fournie par l'objet [DocumentBase](../../com.aspose.words/documentbase/).

Cependant, lorsque vous devez importer des nœuds d'un document à un autre plusieurs fois, il est préférable d'utiliser la classe [NodeImporter](../../com.aspose.words/nodeimporter/). La classe [NodeImporter](../../com.aspose.words/nodeimporter/) permet de minimiser le nombre de styles et de listes créés dans le document de destination.

Copier ou déplacer des fragments d'un document Microsoft Word à un autre présente un certain nombre de défis techniques pour Aspose.Words. Dans un document Word, les styles et la mise en forme des listes sont stockés de façon centralisée, séparément du texte du document. Les paragraphes et les portions de texte ne font qu’y référencer les styles par des identifiants uniques internes.

Les défis proviennent du fait que les styles et les listes diffèrent d'un document à l'autre. Par exemple, pour copier un paragraphe formaté avec le style Titre 1 d'un document à un autre, plusieurs éléments doivent être pris en compte : décider s'il faut copier le style Titre 1 du document source vers le document de destination, cloner le paragraphe, mettre à jour le paragraphe cloné afin qu’il fasse référence au bon style Titre 1 dans le document de destination. Si le style doit être copié, tous les styles qu’il référence (basés sur le style et le style du paragraphe suivant) doivent être analysés et éventuellement copiés également, etc. Des problèmes similaires existent lors de la copie de paragraphes à puces ou numérotés parce que Microsoft Word stocke les définitions de listes séparément du texte.

La classe [NodeImporter](../../com.aspose.words/nodeimporter/) est comme un contexte, qui conserve les « tables de traduction » pendant l'importation. Elle traduit correctement les styles et les listes entre les documents source et destination.

 **Examples:** 

Montre comment insérer le contenu d'un document dans un signet d'un autre document.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Initialise une nouvelle instance de cette classe. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Importe un nœud d'un document vers un autre. |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Importe un nœud d'un document vers un autre.

 **Remarks:** 

L'importation d'un nœud crée une copie du nœud source appartenant au document d'importation. Le nœud retourné n'a pas de parent. Le nœud source n'est pas modifié ni supprimé du document original.

Avant qu'un nœud provenant d'un autre document puisse être inséré dans ce document, il doit être importé. Pendant l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Après que le nœud a été importé, il peut être inséré à l'endroit approprié du document en utilisant [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) ou [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

Si le nœud source appartient déjà au document de destination, alors un clone profond du nœud source est simplement créé.

 **Examples:** 

Montre comment insérer le contenu d'un document dans un signet d'un autre document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | Le nœud à importer. |
| isImportChildren | boolean | true pour importer tous les nœuds enfants de façon récursive ; sinon, false. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
