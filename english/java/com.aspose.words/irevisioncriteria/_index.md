---
title: IRevisionCriteria
linktitle: IRevisionCriteria
second_title: Aspose.Words for Java
description: Implement this interface if you want to control when certain Revision should be accepted/rejected or not by the RevisionCollection.acceptcom.aspose.words.IRevisionCriteria/ RevisionCollection.rejectcom.aspose.words.IRevisionCriteria methods in Java.
type: docs
weight: 773
url: /java/com.aspose.words/irevisioncriteria/
---
```
public interface IRevisionCriteria
```

Implement this interface if you want to control when certain [Revision](../../com.aspose.words/revision/) should be accepted/rejected or not by the [RevisionCollection.accept(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria)/ [RevisionCollection.reject(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria) methods.

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
## Methods

| Method | Description |
| --- | --- |
| [isMatch(Revision revision)](#isMatch-com.aspose.words.Revision) | Checks whether or not specified  revision  matches criteria. |
### isMatch(Revision revision) {#isMatch-com.aspose.words.Revision}
```
public abstract boolean isMatch(Revision revision)
```


Checks whether or not specified  revision  matches criteria.

 **Remarks:** 

The method implementation should not accept/reject the revision or modify it in any way due to unexpected results.

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
| revision | [Revision](../../com.aspose.words/revision/) | The [Revision](../../com.aspose.words/revision/) instance to match criteria. |

**Returns:**
boolean -  True  if the  revision  matches criteria, otherwise  False .
