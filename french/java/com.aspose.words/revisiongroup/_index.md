---
title: "RevisionGroup"
linktitle: "RevisionGroup"
second_title: "Aspose.Words pour Java"
description: "Représente un groupe d'objets Revision séquentiels en Java."
type: docs
weight: 582
url: /fr/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Représente un groupe d'objets [Revision](../../com.aspose.words/revision/) séquentiels.

Pour en savoir plus, consultez l'article de documentation [ Track Changes in a Document ][Track Changes in a Document].

 **Examples:** 

Montre comment imprimer les informations sur un groupe de révisions dans un document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAuthor()](#getAuthor) | Obtient l'auteur de ce groupe de révisions. |
| [getRevisionType()](#getRevisionType) | Obtient le type de révisions incluses dans ce groupe. |
| [getText()](#getText) | Renvoie le texte inséré/supprimé/déplacé ou la description d'un changement de format. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Obtient l'auteur de ce groupe de révisions.

 **Examples:** 

Montre comment imprimer les informations sur un groupe de révisions dans un document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - L'auteur de ce groupe de révisions.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Obtient le type de révisions incluses dans ce groupe.

 **Examples:** 

Montre comment imprimer les informations sur un groupe de révisions dans un document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - Le type de révisions incluses dans ce groupe. La valeur retournée est l'une des constantes [RevisionType](../../com.aspose.words/revisiontype/).
### getText() {#getText}
```
public String getText()
```


Renvoie le texte inséré/supprimé/déplacé ou la description d'un changement de format.

 **Examples:** 

Montre comment imprimer les informations sur un groupe de révisions dans un document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Texte inséré/supprimé/déplacé ou description d'un changement de format.
