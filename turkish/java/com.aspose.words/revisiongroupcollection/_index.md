---
title: "RevisionGroupCollection"
linktitle: "RevisionGroupCollection"
second_title: "Aspose.Words Java için"
description: "Java'da belgede revizyon gruplarını temsil eden RevisionGroup nesnelerinin bir koleksiyonu."
type: docs
weight: 583
url: /tr/java/com.aspose.words/revisiongroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class RevisionGroupCollection implements Iterable
```

Belgedeki revizyon gruplarını temsil eden [RevisionGroup](../../com.aspose.words/revisiongroup/) nesnelerinin bir koleksiyonu.

Daha fazla bilgi için, [ Track Changes in a Document ][Track Changes in a Document] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belgedeki mevcut revizyon gruplarını almak için [RevisionCollection.getGroups()](../../com.aspose.words/revisioncollection/\#getGroups) özelliğini kullanın.

 **Examples:** 

Bir belgede revizyon grubuyla ilgili bilgilerin nasıl yazdırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

Bir belgede revizyon grubunu nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 RevisionGroup revisionGroup = doc.getRevisions().getGroups().get(0);
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen dizindeki bir revizyon grubunu döndürür. |
| [getCount()](#getCount) | Koleksiyondaki revizyon gruplarının sayısını döndürür. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
### get(int index) {#get-int}
```
public RevisionGroup get(int index)
```


Belirtilen dizindeki bir revizyon grubunu döndürür.

 **Examples:** 

Bir belgede revizyon grubunu nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 RevisionGroup revisionGroup = doc.getRevisions().getGroups().get(0);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[RevisionGroup](../../com.aspose.words/revisiongroup/) - A revision group at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki revizyon gruplarının sayısını döndürür.

 **Examples:** 

Bir belgede revizyon grubuyla ilgili bilgilerin nasıl yazdırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - Koleksiyondaki revizyon gruplarının sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

 **Examples:** 

Bir belgenin revizyon koleksiyonuyla nasıl çalışılacağını gösterir.

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
