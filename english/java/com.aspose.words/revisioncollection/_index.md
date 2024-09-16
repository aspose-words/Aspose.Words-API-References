---
title: RevisionCollection
linktitle: RevisionCollection
second_title: Aspose.Words for Java
description: A collection of Revision objects that represent revisions in the document in Java.
type: docs
weight: 539
url: /java/com.aspose.words/revisioncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionCollection implements Iterable
```

A collection of [Revision](../../com.aspose.words/revision/) objects that represent revisions in the document.

To learn more, visit the [ Track Changes in a Document ][Track Changes in a Document] documentation article.

 **Remarks:** 

You do not create instances of this class directly. Use the [Document.getRevisions()](../../com.aspose.words/document/\#getRevisions) property to get revisions present in a document.

 **Examples:** 

Shows how to work with revisions in a document.

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


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Methods

| Method | Description |
| --- | --- |
| [accept(IRevisionCriteria criteria)](#accept-com.aspose.words.IRevisionCriteria) | Accepts revisions that match specified criteria. |
| [acceptAll()](#acceptAll) | Accepts all revisions in this collection. |
| [get(int index)](#get-int) | Returns a [Revision](../../com.aspose.words/revision/) at the specified index. |
| [getCount()](#getCount) | Returns the number of revisions in the collection. |
| [getGroups()](#getGroups) | Collection of revision groups. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [reject(IRevisionCriteria criteria)](#reject-com.aspose.words.IRevisionCriteria) | Rejects revisions that match specified criteria. |
| [rejectAll()](#rejectAll) | Rejects all revisions in this collection. |
### accept(IRevisionCriteria criteria) {#accept-com.aspose.words.IRevisionCriteria}
```
public int accept(IRevisionCriteria criteria)
```


Accepts revisions that match specified criteria.

 **Examples:** 

Shows how to accept or reject revision based on criteria.

```

 public void revisionSpecifiedCriteria() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.write("This does not count as a revision. ");

     // To register our edits as revisions, we need to declare an author, and then start tracking them.
     doc.startTrackRevisions("John Doe", new Date());
     builder.write("This is insertion revision #1. ");
     doc.stopTrackRevisions();

     doc.startTrackRevisions("Jane Doe", new Date());
     builder.write("This is insertion revision #2. ");
     // Remove a run "This does not count as a revision.".
     doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();
     doc.stopTrackRevisions();

     Assert.assertEquals(3, doc.getRevisions().getCount());
     // We have two revisions from different authors, so we need to accept only one.
     doc.getRevisions().accept(new RevisionCriteria("John Doe", RevisionType.INSERTION));
     Assert.assertEquals(2, doc.getRevisions().getCount());
     // Reject revision with different author name and revision type.
     doc.getRevisions().reject(new RevisionCriteria("Jane Doe", RevisionType.DELETION));
     Assert.assertEquals(1, doc.getRevisions().getCount());

     doc.save(getArtifactsDir() + "Revision.RevisionSpecifiedCriteria.docx");
 }

 /// 
 /// Control when certain revision should be accepted/rejected.
 /// 
 public static class RevisionCriteria implements IRevisionCriteria
 {
     private String AuthorName;
     private int _RevisionType;

     public RevisionCriteria(String authorName, int revisionType)
     {
         AuthorName = authorName;
         _RevisionType = revisionType;
     }

     public boolean isMatch(Revision revision)
     {
         return AuthorName.equals(revision.getAuthor()) && revision.getRevisionType() == _RevisionType;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| criteria | [IRevisionCriteria](../../com.aspose.words/irevisioncriteria/) | The [IRevisionCriteria](../../com.aspose.words/irevisioncriteria/) implementation. |

**Returns:**
int - The count of accepted revisions.
### acceptAll() {#acceptAll}
```
public void acceptAll()
```


Accepts all revisions in this collection.

 **Examples:** 

Shows how to compare documents.

```

 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);
 builder.writeln("This is the original document.");

 Document docEdited = new Document();
 builder = new DocumentBuilder(docEdited);
 builder.writeln("This is the edited document.");

 // Comparing documents with revisions will throw an exception.
 if (docOriginal.getRevisions().getCount() == 0 && docEdited.getRevisions().getCount() == 0)
     docOriginal.compare(docEdited, "authorName", new Date());

 // After the comparison, the original document will gain a new revision
 // for every element that is different in the edited document.
 for (Revision r : docOriginal.getRevisions())
 {
     System.out.println("Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
     System.out.println("\tChanged text: \"{r.ParentNode.GetText()}\"");
 }

 // Accepting these revisions will transform the original document into the edited document.
 docOriginal.getRevisions().acceptAll();

 Assert.assertEquals(docOriginal.getText(), docEdited.getText());
 
```

### get(int index) {#get-int}
```
public Revision get(int index)
```


Returns a [Revision](../../com.aspose.words/revision/) at the specified index.

 **Remarks:** 

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

 **Examples:** 

Shows how to work with revisions in a document.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Revision](../../com.aspose.words/revision/) - A [Revision](../../com.aspose.words/revision/) at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of revisions in the collection.

 **Examples:** 

Shows how to work with revisions in a document.

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

**Returns:**
int - The number of revisions in the collection.
### getGroups() {#getGroups}
```
public RevisionGroupCollection getGroups()
```


Collection of revision groups.

 **Examples:** 

Shows how to work with a document's collection of revisions.

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
[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection/) - The corresponding [RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection/) value.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

 **Examples:** 

Shows how to work with a document's collection of revisions.

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
### reject(IRevisionCriteria criteria) {#reject-com.aspose.words.IRevisionCriteria}
```
public int reject(IRevisionCriteria criteria)
```


Rejects revisions that match specified criteria.

 **Examples:** 

Shows how to accept or reject revision based on criteria.

```

 public void revisionSpecifiedCriteria() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.write("This does not count as a revision. ");

     // To register our edits as revisions, we need to declare an author, and then start tracking them.
     doc.startTrackRevisions("John Doe", new Date());
     builder.write("This is insertion revision #1. ");
     doc.stopTrackRevisions();

     doc.startTrackRevisions("Jane Doe", new Date());
     builder.write("This is insertion revision #2. ");
     // Remove a run "This does not count as a revision.".
     doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();
     doc.stopTrackRevisions();

     Assert.assertEquals(3, doc.getRevisions().getCount());
     // We have two revisions from different authors, so we need to accept only one.
     doc.getRevisions().accept(new RevisionCriteria("John Doe", RevisionType.INSERTION));
     Assert.assertEquals(2, doc.getRevisions().getCount());
     // Reject revision with different author name and revision type.
     doc.getRevisions().reject(new RevisionCriteria("Jane Doe", RevisionType.DELETION));
     Assert.assertEquals(1, doc.getRevisions().getCount());

     doc.save(getArtifactsDir() + "Revision.RevisionSpecifiedCriteria.docx");
 }

 /// 
 /// Control when certain revision should be accepted/rejected.
 /// 
 public static class RevisionCriteria implements IRevisionCriteria
 {
     private String AuthorName;
     private int _RevisionType;

     public RevisionCriteria(String authorName, int revisionType)
     {
         AuthorName = authorName;
         _RevisionType = revisionType;
     }

     public boolean isMatch(Revision revision)
     {
         return AuthorName.equals(revision.getAuthor()) && revision.getRevisionType() == _RevisionType;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| criteria | [IRevisionCriteria](../../com.aspose.words/irevisioncriteria/) | The [IRevisionCriteria](../../com.aspose.words/irevisioncriteria/) implementation. |

**Returns:**
int - The count of rejected revisions.
### rejectAll() {#rejectAll}
```
public void rejectAll()
```


Rejects all revisions in this collection.

 **Examples:** 

Shows how to work with a document's collection of revisions.

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

