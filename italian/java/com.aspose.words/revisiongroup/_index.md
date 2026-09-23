---
title: "RevisionGroup"
linktitle: "RevisionGroup"
second_title: "Aspose.Words per Java"
description: "Rappresenta un gruppo di oggetti Revision sequenziali in Java."
type: docs
weight: 582
url: /it/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Rappresenta un gruppo di oggetti [Revision](../../com.aspose.words/revision/) sequenziali.

Per saperne di più, visita l'articolo di documentazione [ Track Changes in a Document ][Track Changes in a Document].

 **Examples:** 

Mostra come stampare informazioni su un gruppo di revisioni in un documento.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAuthor()](#getAuthor) | Ottiene l'autore di questo gruppo di revisioni. |
| [getRevisionType()](#getRevisionType) | Ottiene il tipo di revisioni incluse in questo gruppo. |
| [getText()](#getText) | Restituisce il testo inserito/eliminato/spostato o la descrizione della modifica di formato. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Ottiene l'autore di questo gruppo di revisioni.

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
java.lang.String - L'autore di questo gruppo di revisioni.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Ottiene il tipo di revisioni incluse in questo gruppo.

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
int - Il tipo di revisioni incluse in questo gruppo. Il valore restituito è uno dei costanti di [RevisionType](../../com.aspose.words/revisiontype/).
### getText() {#getText}
```
public String getText()
```


Restituisce il testo inserito/eliminato/spostato o la descrizione della modifica di formato.

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
java.lang.String - Testo inserito/eliminato/spostato o descrizione della modifica di formato.
