---
title: "RevisionGroupCollection"
linktitle: "RevisionGroupCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di oggetti RevisionGroup che rappresentano i gruppi di revisione nel documento in Java."
type: docs
weight: 583
url: /it/java/com.aspose.words/revisiongroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionGroupCollection implements Iterable
```

Una raccolta di oggetti [RevisionGroup](../../com.aspose.words/revisiongroup/) che rappresentano i gruppi di revisione nel documento.

Per saperne di più, visita l'articolo di documentazione [ Track Changes in a Document ][Track Changes in a Document].

 **Remarks:** 

Non si creano istanze di questa classe direttamente. Utilizzare la proprietà [RevisionCollection.getGroups()](../../com.aspose.words/revisioncollection/\#getGroups) per ottenere i gruppi di revisione presenti in un documento.

 **Examples:** 

Mostra come stampare informazioni su un gruppo di revisioni in un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

Mostra come ottenere un gruppo di revisioni in un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 RevisionGroup revisionGroup = doc.getRevisions().getGroups().get(0);
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Restituisce un gruppo di revisioni all'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di gruppi di revisione nella raccolta. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
### get(int index) {#get-int}
```
public RevisionGroup get(int index)
```


Restituisce un gruppo di revisioni all'indice specificato.

 **Examples:** 

Mostra come ottenere un gruppo di revisioni in un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 RevisionGroup revisionGroup = doc.getRevisions().getGroups().get(0);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[RevisionGroup](../../com.aspose.words/revisiongroup/) - A revision group at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di gruppi di revisione nella raccolta.

 **Examples:** 

Mostra come stampare informazioni su un gruppo di revisioni in un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - Il numero di gruppi di revisione nella raccolta.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

 **Examples:** 

Mostra come lavorare con la raccolta di revisioni di un documento.

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
