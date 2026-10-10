---
title: "مجموعة المراجعات"
linktitle: "مجموعة المراجعات"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من كائنات Revision المتسلسلة في Java."
type: docs
weight: 582
url: /ar/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

يمثل مجموعة من كائنات [Revision](../../com.aspose.words/revision/) المتسلسلة.

لمزيد من المعلومات، زر مقالة الوثائق [ Track Changes in a Document ][Track Changes in a Document].

 **Examples:** 

يوضح كيفية طباعة معلومات حول مجموعة من المراجعات في مستند.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAuthor()](#getAuthor) | يحصل على مؤلف مجموعة المراجعات هذه. |
| [getRevisionType()](#getRevisionType) | يحصل على نوع المراجعات المتضمنة في هذه المجموعة. |
| [getText()](#getText) | يعيد النص المُدرج/المحذوف/المنقَل أو وصف تغيير التنسيق. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


يحصل على مؤلف مجموعة المراجعات هذه.

 **Examples:** 

يوضح كيفية طباعة معلومات حول مجموعة من المراجعات في مستند.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - مؤلف مجموعة المراجعات هذه.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


يحصل على نوع المراجعات المتضمنة في هذه المجموعة.

 **Examples:** 

يوضح كيفية طباعة معلومات حول مجموعة من المراجعات في مستند.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - نوع المراجعات المتضمنة في هذه المجموعة. القيمة المرجعة هي واحدة من ثوابت [RevisionType](../../com.aspose.words/revisiontype/).
### getText() {#getText}
```
public String getText()
```


يعيد النص المُدرج/المحذوف/المنقَل أو وصف تغيير التنسيق.

 **Examples:** 

يوضح كيفية طباعة معلومات حول مجموعة من المراجعات في مستند.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - النص المُدرج/المحذوف/المنقَل أو وصف تغيير التنسيق.
