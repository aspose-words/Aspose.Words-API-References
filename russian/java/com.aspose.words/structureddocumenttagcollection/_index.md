---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words для Java"
description: "Коллекция экземпляров IStructuredDocumentTag, представляющих структурные теги документа в указанном диапазоне в Java."
type: docs
weight: 638
url: /ru/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

Коллекция экземпляров [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/), представляющих структурные теги документа в указанном диапазоне.

Чтобы узнать больше, посетите статью документации [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Показывает, как получить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Методы

| Метод | Описание |
| --- | --- |
| [get(int index)](#get-int) | Возвращает структурный тег документа по указанному индексу. |
| [getById(int id)](#getById-int) | Возвращает структурный тег документа по идентификатору. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Возвращает первый найденный в коллекции структурный тег документа с указанным тегом. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Возвращает первый найденный в коллекции структурный тег документа с указанным заголовком. |
| [getCount()](#getCount) | Возвращает количество структурных тегов документа в коллекции. |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
| [remove(int id)](#remove-int) | Удаляет структурный тег документа с указанным идентификатором. |
| [removeAt(int index)](#removeAt-int) | Удаляет структурный тег документа по указанному индексу. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Возвращает структурный тег документа по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс в коллекции. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Возвращает структурный тег документа по идентификатору.

 **Remarks:** 

Возвращает null, если структурный тег документа с указанным идентификатором не найден.

 **Examples:** 

Показывает, как получить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| id | int | Идентификатор структурного тега документа. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Возвращает первый найденный в коллекции структурный тег документа с указанным тегом.

 **Remarks:** 

Возвращает null, если структурный тег документа с указанным тегом не найден.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| тег | java.lang.String | Тег структурированного тега документа. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Возвращает первый найденный в коллекции структурный тег документа с указанным заголовком.

 **Remarks:** 

Возвращает null, если структурированный тег документа с указанным заголовком не найден.

 **Examples:** 

Показывает, как получить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| заголовок | java.lang.String | Заголовок структурированного тега документа. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Возвращает количество структурных тегов документа в коллекции.

**Returns:**
int — количество структурированных тегов документа в коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Удаляет структурный тег документа с указанным идентификатором.

 **Examples:** 

Показывает, как удалить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 StructuredDocumentTagCollection structuredDocumentTags = doc.getRange().getStructuredDocumentTags();
 IStructuredDocumentTag sdt;
 for (int i = 0; i < structuredDocumentTags.getCount(); i++)
 {
     sdt = structuredDocumentTags.get(i);
     System.out.println(sdt.getTitle());
 }

 sdt = structuredDocumentTags.getById(1691867797);
 Assert.assertEquals(1691867797, sdt.getId());

 Assert.assertEquals(5, structuredDocumentTags.getCount());
 // Remove the structured document tag by Id.
 structuredDocumentTags.remove(1691867797);
 // Remove the structured document tag at position 0.
 structuredDocumentTags.removeAt(0);
 Assert.assertEquals(3, structuredDocumentTags.getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| id | int | Идентификатор структурного тега документа. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет структурный тег документа по указанному индексу.

 **Examples:** 

Показывает, как удалить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 StructuredDocumentTagCollection structuredDocumentTags = doc.getRange().getStructuredDocumentTags();
 IStructuredDocumentTag sdt;
 for (int i = 0; i < structuredDocumentTags.getCount(); i++)
 {
     sdt = structuredDocumentTags.get(i);
     System.out.println(sdt.getTitle());
 }

 sdt = structuredDocumentTags.getById(1691867797);
 Assert.assertEquals(1691867797, sdt.getId());

 Assert.assertEquals(5, structuredDocumentTags.getCount());
 // Remove the structured document tag by Id.
 structuredDocumentTags.remove(1691867797);
 // Remove the structured document tag at position 0.
 structuredDocumentTags.removeAt(0);
 Assert.assertEquals(3, structuredDocumentTags.getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс в коллекции. |

