---
title: RevisionGroup
linktitle: RevisionGroup
second_title: Aspose.Words for Java
description: Represents a group of sequential Revision objects in Java.
type: docs
weight: 526
url: /java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Represents a group of sequential [Revision](../../com.aspose.words/revision/) objects.

To learn more, visit the [ Track Changes in a Document ][Track Changes in a Document] documentation article.

 **Examples:** 

Shows how to print info about a group of revisions in a document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Methods

| Method | Description |
| --- | --- |
| [getAuthor()](#getAuthor) | Gets the author of this revision group. |
| [getRevisionType()](#getRevisionType) | Gets the type of revisions included in this group. |
| [getText()](#getText) | Returns inserted/deleted/moved text or description of format change. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Gets the author of this revision group.

 **Examples:** 

Shows how to print info about a group of revisions in a document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - The author of this revision group.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Gets the type of revisions included in this group.

 **Examples:** 

Shows how to print info about a group of revisions in a document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - The type of revisions included in this group. The returned value is one of [RevisionType](../../com.aspose.words/revisiontype/) constants.
### getText() {#getText}
```
public String getText()
```


Returns inserted/deleted/moved text or description of format change.

 **Examples:** 

Shows how to print info about a group of revisions in a document.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Inserted/deleted/moved text or description of format change.
