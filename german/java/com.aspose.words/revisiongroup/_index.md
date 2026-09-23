---
title: "RevisionGroup"
linktitle: "RevisionGroup"
second_title: "Aspose.Words für Java"
description: "Stellt eine Gruppe von aufeinanderfolgenden Revision-Objekten in Java dar."
type: docs
weight: 582
url: /de/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Stellt eine Gruppe von aufeinanderfolgenden [Revision](../../com.aspose.words/revision/) Objekten dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Track Changes in a Document ][Track Changes in a Document].

 **Examples:** 

Zeigt, wie Informationen über eine Gruppe von Revisionen in einem Dokument ausgegeben werden.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAuthor()](#getAuthor) | Liest den Autor dieser Revisionsgruppe. |
| [getRevisionType()](#getRevisionType) | Liest den Typ der in dieser Gruppe enthaltenen Revisionen. |
| [getText()](#getText) | Gibt eingefügten/gelöschten/verschobenen Text oder die Beschreibung einer Formatänderung zurück. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Liest den Autor dieser Revisionsgruppe.

 **Examples:** 

Zeigt, wie Informationen über eine Gruppe von Revisionen in einem Dokument ausgegeben werden.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Der Autor dieser Revisionsgruppe.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Liest den Typ der in dieser Gruppe enthaltenen Revisionen.

 **Examples:** 

Zeigt, wie Informationen über eine Gruppe von Revisionen in einem Dokument ausgegeben werden.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - Der Typ der in dieser Gruppe enthaltenen Revisionen. Der zurückgegebene Wert ist einer der [RevisionType](../../com.aspose.words/revisiontype/) Konstanten.
### getText() {#getText}
```
public String getText()
```


Gibt eingefügten/gelöschten/verschobenen Text oder die Beschreibung einer Formatänderung zurück.

 **Examples:** 

Zeigt, wie Informationen über eine Gruppe von Revisionen in einem Dokument ausgegeben werden.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Eingefügter/gelöschter/verschobener Text oder Beschreibung einer Formatänderung.
