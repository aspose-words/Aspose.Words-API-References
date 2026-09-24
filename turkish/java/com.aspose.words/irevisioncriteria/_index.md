---
title: "IRevisionCriteria"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words Java için"
description: "Bu arayüzü, belirli bir Revision'ın Java'da RevisionCollection.acceptcom.aspose.words.IRevisionCriteria / RevisionCollection.rejectcom.aspose.words.IRevisionCriteria yöntemleriyle kabul edilip edilmeyeceğini kontrol etmek istiyorsanız uygulayın."
type: docs
weight: 784
url: /tr/java/com.aspose.words/irevisioncriteria/
---
```
public interface IRevisionCriteria
```

Bu arayüzü, belirli bir [Revision](../../com.aspose.words/revision/) öğesinin [RevisionCollection.accept(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria) / [RevisionCollection.reject(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria) yöntemleriyle kabul edilip edilmeyeceğini kontrol etmek istiyorsanız uygulayın.

 **Examples:** 

Kriterlere göre revizyonun nasıl kabul edileceğini veya reddedileceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [isMatch(Revision revision)](#isMatch-com.aspose.words.Revision) | Belirtilen revizyonun kriterlerle eşleşip eşleşmediğini kontrol eder. |
### isMatch(Revision revision) {#isMatch-com.aspose.words.Revision}
```
public abstract boolean isMatch(Revision revision)
```


Belirtilen revizyonun kriterlerle eşleşip eşleşmediğini kontrol eder.

 **Remarks:** 

Yöntem uygulaması, beklenmeyen sonuçlar nedeniyle revizyonu kabul/ret etmemeli veya herhangi bir şekilde değiştirmemelidir.

 **Examples:** 

Kriterlere göre revizyonun nasıl kabul edileceğini veya reddedileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| revision | [Revision](../../com.aspose.words/revision/) | Kriterlerle eşleşecek [Revision](../../com.aspose.words/revision/) örneği. |

**Returns:**
boolean -  Revizyon kriterlerle eşleşiyorsa True, aksi takdirde False .
