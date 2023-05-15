---
title: NodeImporter
linktitle: NodeImporter
second_title: Aspose.Words for Java
description: Allows to efficiently perform repeated import of nodes from one document to another in Java.
type: docs
weight: 422
url: /java/com.aspose.words/nodeimporter/
---

**Inheritance:**
java.lang.Object
```
public class NodeImporter
```

Allows to efficiently perform repeated import of nodes from one document to another.

To learn more, visit the [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] documentation article.

 **Remarks:** 

Aspose.Words provides functionality for easy copying and moving fragments between Microsoft Word documents. This is known as "importing nodes". Before you can insert a fragment from one document into another, you need to "import" it. Importing creates a deep clone of the original node, ready to be inserted into the destination document.

The simplest way to import a node is to use the [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) method provided by the [DocumentBase](../../com.aspose.words/documentbase/) object.

However, when you need to import nodes from one document to another multiple times, it is better to use the [NodeImporter](../../com.aspose.words/nodeimporter/) class. The [NodeImporter](../../com.aspose.words/nodeimporter/) class allows to minimize the number of styles and lists created in the destination document.

Copying or moving fragments from one Microsoft Word document to another presents a number of technical challenges for Aspose.Words. In a Word document, styles and list formatting are stored centrally, separately from the text of the document. The paragraphs and runs of text merely reference the styles by internal unique identifiers.

The challenges arise from the fact that styles and lists are different in different documents. For example, to copy a paragraph formatted with the Heading 1 style from one document to another, a number of things must be taken into account: decide whether to copy the Heading 1 style from the source document to the destination document, clone the paragraph, update the cloned paragraph so it refers to the correct Heading 1 style in the destination document. If the style had to be copied, all the styles that it references (based on style and next paragraph style) should be analyzed and possibly copied too and so on. Similar issues exist when copying bulleted or numbered paragraphs because Microsoft Word stores list definitions separately from text.

The [NodeImporter](../../com.aspose.words/nodeimporter/) class is like a context, that holds the "translation tables" during the import. It correctly translates between styles and lists in the source and destination documents.

 **Examples:** 

Shows how to insert the contents of one document to a bookmark in another document.

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
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int) | Initializes a new instance of this class. |
| [NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Imports a node from one document into another. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |

### NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#NodeImporter-com.aspose.words.DocumentBase-com.aspose.words.DocumentBase-int-com.aspose.words.ImportFormatOptions}
```
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| dstDoc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Imports a node from one document into another.

 **Remarks:** 

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) or [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

 **Examples:** 

Shows how to insert the contents of one document to a bookmark in another document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | The node to import. |
| isImportChildren | boolean |  true  to import all child nodes recursively; otherwise,  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned, imported node. The node belongs to the destination document, but has no parent.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

