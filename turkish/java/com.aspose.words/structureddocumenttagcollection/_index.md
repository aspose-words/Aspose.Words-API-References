---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words Java için"
description: "Java'da belirtilen aralıktaki yapılandırılmış belge etiketlerini temsil eden IStructuredDocumentTag örneklerinden oluşan bir koleksiyon."
type: docs
weight: 638
url: /tr/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

Belirtilen aralıktaki yapılandırılmış belge etiketlerini temsil eden [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) örneklerinden oluşan bir koleksiyon.

Daha fazla bilgi için, [ Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü ][Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen indeksteki yapılandırılmış belge etiketini döndürür. |
| [getById(int id)](#getById-int) | Yapılandırılmış belge etiketini tanımlayıcıyla döndürür. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Koleksiyonda belirtilen etiketle karşılaşılan ilk yapılandırılmış belge etiketini döndürür. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Koleksiyonda belirtilen başlıkla karşılaşılan ilk yapılandırılmış belge etiketini döndürür. |
| [getCount()](#getCount) | Koleksiyondaki yapılandırılmış belge etiketlerinin sayısını döndürür. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
| [remove(int id)](#remove-int) | Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketini kaldırır. |
| [removeAt(int index)](#removeAt-int) | Belirtilen indeksteki bir yapılandırılmış belge etiketini kaldırır. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Belirtilen indeksteki yapılandırılmış belge etiketini döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Koleksiyona ait bir indeks. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Yapılandırılmış belge etiketini tanımlayıcıyla döndürür.

 **Remarks:** 

Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketi bulunamazsa null döndürür.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| id | int | Yapılandırılmış belge etiketi tanımlayıcısı. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Koleksiyonda belirtilen etiketle karşılaşılan ilk yapılandırılmış belge etiketini döndürür.

 **Remarks:** 

Belirtilen etiketle yapılandırılmış belge etiketi bulunamazsa null döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| etiket | java.lang.String | Yapılandırılmış belge etiketinin etiketi. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Koleksiyonda belirtilen başlıkla karşılaşılan ilk yapılandırılmış belge etiketini döndürür.

 **Remarks:** 

Belirtilen başlığa sahip yapılandırılmış belge etiketi bulunamazsa null döndürür.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| başlık | java.lang.String | Yapılandırılmış belge etiketinin başlığı. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyondaki yapılandırılmış belge etiketlerinin sayısını döndürür.

**Returns:**
int - Koleksiyondaki yapılandırılmış belge etiketlerinin sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Belirtilen tanımlayıcıya sahip yapılandırılmış belge etiketini kaldırır.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl kaldırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| id | int | Yapılandırılmış belge etiketi tanımlayıcısı. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Belirtilen indeksteki bir yapılandırılmış belge etiketini kaldırır.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl kaldırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Koleksiyona ait bir indeks. |

