---
title: "IRevisionCriteria"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie steuern möchten, wann bestimmte Revisionen von den Methoden RevisionCollection.acceptcom.aspose.words.IRevisionCriteria / RevisionCollection.rejectcom.aspose.words.IRevisionCriteria in Java akzeptiert bzw. abgelehnt werden sollen."
type: docs
weight: 784
url: /de/java/com.aspose.words/irevisioncriteria/
---
```
public interface IRevisionCriteria
```

Implementieren Sie dieses Interface, wenn Sie steuern möchten, wann bestimmte [Revision](../../com.aspose.words/revision/) akzeptiert/abgelehnt werden sollen oder nicht durch die Methoden [RevisionCollection.accept(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria)/ [RevisionCollection.reject(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria).

 **Examples:** 

Zeigt, wie man Revisionen basierend auf Kriterien akzeptiert oder ablehnt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [isMatch(Revision revision)](#isMatch-com.aspose.words.Revision) | Überprüft, ob die angegebene Revision den Kriterien entspricht oder nicht. |
### isMatch(Revision revision) {#isMatch-com.aspose.words.Revision}
```
public abstract boolean isMatch(Revision revision)
```


Überprüft, ob die angegebene Revision den Kriterien entspricht oder nicht.

 **Remarks:** 

Die Implementierung der Methode sollte die Revision nicht akzeptieren/ablehnen oder sie in irgendeiner Weise ändern, um unerwartete Ergebnisse zu vermeiden.

 **Examples:** 

Zeigt, wie man Revisionen basierend auf Kriterien akzeptiert oder ablehnt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revision | [Revision](../../com.aspose.words/revision/) | Die [Revision](../../com.aspose.words/revision/) Instanz, die mit den Kriterien abgeglichen werden soll. |

**Returns:**
boolean -  True  wenn die  Revision  den Kriterien entspricht, andernfalls  False .
