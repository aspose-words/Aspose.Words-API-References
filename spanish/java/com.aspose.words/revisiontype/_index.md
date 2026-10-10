---
title: "RevisionType"
linktitle: "RevisionType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de cambio que se rastrea en Revision en Java."
type: docs
weight: 586
url: /es/java/com.aspose.words/revisiontype/
---

**Inheritance:**
java.lang.Object
```
public class RevisionType
```

Especifica el tipo de cambio que se rastrea en [Revision](../../com.aspose.words/revision/).

 **Examples:** 

Muestra cómo trabajar con revisiones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normal editing of the document does not count as a revision.
 builder.write("This does not count as a revision. ");

 Assert.assertFalse(doc.hasRevisions());

 // To register our edits as revisions, we need to declare an author, and then start tracking them.
 doc.startTrackRevisions("John Doe", new Date());

 builder.write("This is revision #1. ");

 Assert.assertTrue(doc.hasRevisions());
 Assert.assertEquals(1, doc.getRevisions().getCount());

 // This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
 // The "StartTrackRevisions" method does not affect its value,
 // and the document is tracking revisions programmatically despite it having a value of "false".
 // If we open this document using Microsoft Word, it will not be tracking revisions.
 Assert.assertFalse(doc.getTrackRevisions());

 // We have added text using the document builder, so the first revision is an insertion-type revision.
 Revision revision = doc.getRevisions().get(0);
 Assert.assertEquals("John Doe", revision.getAuthor());
 Assert.assertEquals("This is revision #1. ", revision.getParentNode().getText());
 Assert.assertEquals(RevisionType.INSERTION, revision.getRevisionType());
 Assert.assertEquals(revision.getDateTime().getDate(), new Date().getDate());
 Assert.assertEquals(doc.getRevisions().getGroups().get(0), revision.getGroup());

 // Remove a run to create a deletion-type revision.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();

 // Adding a new revision places it at the beginning of the revision collection.
 Assert.assertEquals(RevisionType.DELETION, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(2, doc.getRevisions().getCount());

 // Insert revisions show up in the document body even before we accept/reject the revision.
 // Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
 // also linger in the document until we accept the revision.
 Assert.assertEquals("This does not count as a revision. This is revision #1.", doc.getText().trim());

 // Accepting the delete revision will remove its parent node from the paragraph text
 // and then remove the collection's revision itself.
 doc.getRevisions().get(0).accept();

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1.", doc.getText().trim());

 builder.writeln("");
 builder.write("This is revision #2.");

 // Now move the node to create a moving revision type.
 Node node = doc.getFirstSection().getBody().getParagraphs().get(1);
 Node endNode = doc.getFirstSection().getBody().getParagraphs().get(1).getNextSibling();
 Node referenceNode = doc.getFirstSection().getBody().getParagraphs().get(0);

 while (node != endNode)
 {
     Node nextNode = node.getNextSibling();
     doc.getFirstSection().getBody().insertBefore(node, referenceNode);
     node = nextNode;
 }

 Assert.assertEquals(RevisionType.MOVING, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(8, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.getText().trim());

 // The moving revision is now at index 1. Reject the revision to discard its contents.
 doc.getRevisions().get(1).reject();

 Assert.assertEquals(6, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1. \rThis is revision #2.", doc.getText().trim());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [DELETION](#DELETION) | El contenido fue eliminado del documento. |
| [FORMAT_CHANGE](#FORMAT-CHANGE) | Se aplicó un cambio de formato al nodo padre. |
| [INSERTION](#INSERTION) | Se insertó contenido nuevo en el documento. |
| [MOVING](#MOVING) | El contenido fue movido en el documento. |
| [STYLE_DEFINITION_CHANGE](#STYLE-DEFINITION-CHANGE) | Se aplicó un cambio de formato al estilo padre. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String revisionTypeName)](#fromName-java.lang.String) |  |
| [getName(int revisionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int revisionType)](#toString-int) |  |
### DELETION {#DELETION}
```
public static int DELETION
```


El contenido fue eliminado del documento.

### FORMAT_CHANGE {#FORMAT-CHANGE}
```
public static int FORMAT_CHANGE
```


Se aplicó un cambio de formato al nodo padre.

### INSERTION {#INSERTION}
```
public static int INSERTION
```


Se insertó contenido nuevo en el documento.

### MOVING {#MOVING}
```
public static int MOVING
```


El contenido fue movido en el documento.

### STYLE_DEFINITION_CHANGE {#STYLE-DEFINITION-CHANGE}
```
public static int STYLE_DEFINITION_CHANGE
```


Se aplicó un cambio de formato al estilo padre.

### length {#length}
```
public static int length
```


### fromName(String revisionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionTypeName | java.lang.String |  |

**Returns:**
int
### getName(int revisionType) {#getName-int}
```
public static String getName(int revisionType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int revisionType) {#toString-int}
```
public static String toString(int revisionType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| revisionType | int |  |

**Returns:**
java.lang.String
