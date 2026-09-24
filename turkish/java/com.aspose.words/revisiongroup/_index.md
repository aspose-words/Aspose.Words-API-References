---
title: "RevisionGroup"
linktitle: "RevisionGroup"
second_title: "Aspose.Words Java için"
description: "Java'da sıralı Revision nesnelerinden oluşan bir grup temsil eder."
type: docs
weight: 582
url: /tr/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Sıralı [Revision](../../com.aspose.words/revision/) nesnelerinden oluşan bir grup temsil eder.

Daha fazla bilgi için, [ Track Changes in a Document ][Track Changes in a Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgede revizyon grubuyla ilgili bilgilerin nasıl yazdırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAuthor()](#getAuthor) | Bu revizyon grubunun yazarını alır. |
| [getRevisionType()](#getRevisionType) | Bu gruba dahil edilen revizyonların tipini alır. |
| [getText()](#getText) | Ekleme/silme/taşıma metnini veya biçim değişikliği açıklamasını döndürür. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Bu revizyon grubunun yazarını alır.

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
java.lang.String - Bu revizyon grubunun yazarı.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Bu gruba dahil edilen revizyonların tipini alır.

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
int - Bu gruba dahil edilen revizyonların tipi. Döndürülen değer [RevisionType](../../com.aspose.words/revisiontype/) sabitlerinden biridir.
### getText() {#getText}
```
public String getText()
```


Ekleme/silme/taşıma metnini veya biçim değişikliği açıklamasını döndürür.

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
java.lang.String - Ekleme/silme/taşıma metni veya biçim değişikliği açıklaması.
