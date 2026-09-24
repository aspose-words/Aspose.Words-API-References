---
title: "RevisionGroupCollection"
linktitle: "RevisionGroupCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de objetos RevisionGroup que representan grupos de revisiones en el documento en Java."
type: docs
weight: 583
url: /es/java/com.aspose.words/revisiongroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionGroupCollection implements Iterable
```

Una colección de objetos [RevisionGroup](../../com.aspose.words/revisiongroup/) que representan grupos de revisiones en el documento.

Para obtener más información, visite el artículo de documentación [ Track Changes in a Document ][Track Changes in a Document].

 **Remarks:** 

No crea instancias de esta clase directamente. Use la propiedad [RevisionCollection.getGroups()](../../com.aspose.words/revisioncollection/\#getGroups) para obtener los grupos de revisiones presentes en un documento.

 **Examples:** 

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

Muestra cómo obtener un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 RevisionGroup revisionGroup = doc.getRevisions().getGroups().get(0);
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Devuelve un grupo de revisiones en el índice especificado. |
| [getCount()](#getCount) | Devuelve el número de grupos de revisión en la colección. |
| [iterator()](#iterator) | Devuelve un objeto enumerador. |
### get(int index) {#get-int}
```
public RevisionGroup get(int index)
```


Devuelve un grupo de revisiones en el índice especificado.

 **Examples:** 

Muestra cómo obtener un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 RevisionGroup revisionGroup = doc.getRevisions().getGroups().get(0);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[RevisionGroup](../../com.aspose.words/revisiongroup/) - A revision group at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Devuelve el número de grupos de revisión en la colección.

 **Examples:** 

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - El número de grupos de revisión en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto enumerador.

 **Examples:** 

Muestra cómo trabajar con la colección de revisiones de un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");
 RevisionCollection revisions = doc.getRevisions();

 // This collection itself has a collection of revision groups.
 // Each group is a sequence of adjacent revisions.
 System.out.println(MessageFormat.format("{0} revision groups:", revisions.getGroups().getCount()));

 // Iterate over the collection of groups and print the text that the revision concerns.
 Iterator e = revisions.getGroups().iterator();

 while (e.hasNext()) {
     RevisionGroup revisionGroup = e.next();

     System.out.println(MessageFormat.format("\tGroup type \"{0}\", ", revisionGroup.getRevisionType()) +
             MessageFormat.format("author: {0}, contents: [{1}]", revisionGroup.getAuthor(), revisionGroup.getText().trim()));
 }

 // Each Run that a revision affects gets a corresponding Revision object.
 // The revisions' collection is considerably larger than the condensed form we printed above,
 // depending on how many Runs we have segmented the document into during Microsoft Word editing.
 System.out.println("\n{revisions.Count} revisions:");

 Iterator e1 = revisions.iterator();

 while (e1.hasNext()) {
     Revision revision = e1.next();

     // A StyleDefinitionChange strictly affects styles and not document nodes. This means the "ParentStyle"
     // property will always be in use, while the ParentNode will always be null.
     // Since all other changes affect nodes, ParentNode will conversely be in use, and ParentStyle will be null.
     if (revision.getRevisionType() == RevisionType.STYLE_DEFINITION_CHANGE) {
         System.out.println(MessageFormat.format("\tRevision type \"{0}\", ", revision.getRevisionType()) +
                 MessageFormat.format("author: {0}, style: [{1}]", revision.getAuthor(), revision.getParentStyle().getName()));
     } else {
         System.out.println(MessageFormat.format("\tRevision type \"{0}\", ", revision.getRevisionType()) +
                 MessageFormat.format("author: {0}, contents: [{1}]", revision.getAuthor(), revision.getParentNode().getText().trim()));
     }
 }

 // Reject all revisions via the collection, reverting the document to its original form.
 revisions.rejectAll();

 Assert.assertEquals(0, revisions.getCount());
 
```

**Returns:**
java.util.Iterator
