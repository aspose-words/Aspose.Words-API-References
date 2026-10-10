---
title: "IRevisionCriteria"
linktitle: "IRevisionCriteria"
second_title: "Aspose.Words for Java"
description: "如果您想控制何时通过 RevisionCollection.acceptcom.aspose.words.IRevisionCriteria/ RevisionCollection.rejectcom.aspose.words.IRevisionCriteria 方法在 Java 中接受或拒绝特定 Revision，请实现此接口。"
type: docs
weight: 784
url: /zh/java/com.aspose.words/irevisioncriteria/
---
```
public interface IRevisionCriteria
```

如果您想控制何时通过 [RevisionCollection.accept(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria) / [RevisionCollection.reject(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria) 方法接受或拒绝特定的 [Revision](../../com.aspose.words/revision/) ，请实现此接口。

 **Examples:** 

展示如何根据条件接受或拒绝修订。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [isMatch(Revision revision)](#isMatch-com.aspose.words.Revision) | 检查指定的 revision 是否符合条件。 |
### isMatch(Revision revision) {#isMatch-com.aspose.words.Revision}
```
public abstract boolean isMatch(Revision revision)
```


检查指定的 revision 是否符合条件。

 **Remarks:** 

方法实现不应接受/拒绝该 revision，也不应以任何方式修改它，以免产生意外结果。

 **Examples:** 

展示如何根据条件接受或拒绝修订。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| revision | [Revision](../../com.aspose.words/revision/) | 用于匹配条件的 [Revision](../../com.aspose.words/revision/) 实例。 |

**Returns:**
boolean - 如果 revision 符合条件则为 True，否则为 False。
