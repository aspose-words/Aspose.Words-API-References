---
title: "RevisionGroup"
linktitle: "RevisionGroup"
second_title: "Aspose.Words для Java"
description: "Представляет группу последовательных объектов Revision в Java."
type: docs
weight: 582
url: /ru/java/com.aspose.words/revisiongroup/
---

**Inheritance:**
java.lang.Object
```
public class RevisionGroup
```

Представляет группу последовательных объектов [Revision](../../com.aspose.words/revision/).

Чтобы узнать больше, посетите статью документации [ Track Changes in a Document ][Track Changes in a Document].

 **Examples:** 

Показывает, как вывести информацию о группе исправлений в документе.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```


[Track Changes in a Document]: https://docs.aspose.com/words/java/track-changes-in-a-document/
## Методы

| Метод | Описание |
| --- | --- |
| [getAuthor()](#getAuthor) | Получает автора этой группы исправлений. |
| [getRevisionType()](#getRevisionType) | Получает тип исправлений, включенных в эту группу. |
| [getText()](#getText) | Возвращает вставленный/удалённый/перемещённый текст или описание изменения формата. |
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Получает автора этой группы исправлений.

 **Examples:** 

Показывает, как вывести информацию о группе исправлений в документе.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Автор этой группы исправлений.
### getRevisionType() {#getRevisionType}
```
public int getRevisionType()
```


Получает тип исправлений, включенных в эту группу.

 **Examples:** 

Показывает, как вывести информацию о группе исправлений в документе.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
int - Тип исправлений, включенных в эту группу. Возвращаемое значение является одной из констант [RevisionType](../../com.aspose.words/revisiontype/).
### getText() {#getText}
```
public String getText()
```


Возвращает вставленный/удалённый/перемещённый текст или описание изменения формата.

 **Examples:** 

Показывает, как вывести информацию о группе исправлений в документе.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Assert.assertEquals(7, doc.getRevisions().getGroups().getCount());

 for (RevisionGroup group : doc.getRevisions().getGroups()) {
     System.out.println(MessageFormat.format("Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group.getAuthor(), group.getRevisionType(), group.getText()));
 }
 
```

**Returns:**
java.lang.String - Вставленный/удалённый/перемещённый текст или описание изменения формата.
