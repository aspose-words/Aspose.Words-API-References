---
title: "IRevisionCriteria"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words per Java"
description: "Implementa questa interfaccia se desideri controllare quando una determinata Revision deve essere accettata/rifiutata o meno dai metodi RevisionCollection.acceptcom.aspose.words.IRevisionCriteria/ RevisionCollection.rejectcom.aspose.words.IRevisionCriteria in Java."
type: docs
weight: 784
url: /it/java/com.aspose.words/irevisioncriteria/
---
```
public interface IRevisionCriteria
```

Implementa questa interfaccia se desideri controllare quando una determinata [Revision](../../com.aspose.words/revision/) deve essere accettata/rifiutata o meno dai metodi [RevisionCollection.accept(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria) / [RevisionCollection.reject(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria).

 **Examples:** 

Mostra come accettare o rifiutare una revisione in base ai criteri.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [isMatch(Revision revision)](#isMatch-com.aspose.words.Revision) | Verifica se la revisione specificata corrisponde o meno ai criteri. |
### isMatch(Revision revision) {#isMatch-com.aspose.words.Revision}
```
public abstract boolean isMatch(Revision revision)
```


Verifica se la revisione specificata corrisponde o meno ai criteri.

 **Remarks:** 

L'implementazione del metodo non dovrebbe accettare/rifiutare la revisione né modificarla in alcun modo a causa di risultati imprevisti.

 **Examples:** 

Mostra come accettare o rifiutare una revisione in base ai criteri.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revision | [Revision](../../com.aspose.words/revision/) | L'istanza di [Revision](../../com.aspose.words/revision/) da confrontare con i criteri. |

**Returns:**
boolean -  True  se la  revisione  corrisponde ai criteri, altrimenti  False .
