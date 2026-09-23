---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words für Java"
description: "Eine Sammlung von IStructuredDocumentTag-Instanzen, die die strukturierten Dokument-Tags im angegebenen Bereich in Java darstellen."
type: docs
weight: 638
url: /de/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

Eine Sammlung von [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) Instanzen, die die strukturierten Dokument-Tags im angegebenen Bereich darstellen.

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Zeigt, wie ein strukturierter Dokumenttag abgerufen wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Gibt das strukturierte Dokument-Tag am angegebenen Index zurück. |
| [getById(int id)](#getById-int) | Gibt das strukturierte Dokument-Tag anhand der Kennung zurück. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Tag gefunden wird. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wird. |
| [getCount()](#getCount) | Gibt die Anzahl der strukturierten Dokument-Tags in der Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
| [remove(int id)](#remove-int) | Entfernt das strukturierte Dokument-Tag mit der angegebenen Kennung. |
| [removeAt(int index)](#removeAt-int) | Entfernt ein strukturiertes Dokument-Tag am angegebenen Index. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Gibt das strukturierte Dokument-Tag am angegebenen Index zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Sammlung. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Gibt das strukturierte Dokument-Tag anhand der Kennung zurück.

 **Remarks:** 

Gibt null zurück, wenn das strukturierte Dokument-Tag mit der angegebenen Kennung nicht gefunden werden kann.

 **Examples:** 

Zeigt, wie ein strukturierter Dokumenttag abgerufen wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| id | int | Die Kennung des strukturierten Dokument-Tags. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Tag gefunden wird.

 **Remarks:** 

Gibt null zurück, wenn das strukturierte Dokument-Tag mit dem angegebenen Tag nicht gefunden werden kann.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Tag | java.lang.String | Der Tag des strukturierten Dokument-Tags. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wird.

 **Remarks:** 

Gibt null zurück, wenn das strukturierte Dokument-Tag mit dem angegebenen Titel nicht gefunden werden kann.

 **Examples:** 

Zeigt, wie ein strukturierter Dokumenttag abgerufen wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Titel | java.lang.String | Der Titel des strukturierten Dokument-Tags. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Anzahl der strukturierten Dokument-Tags in der Sammlung zurück.

**Returns:**
int - Die Anzahl der strukturierten Dokument-Tags in der Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Entfernt das strukturierte Dokument-Tag mit der angegebenen Kennung.

 **Examples:** 

Zeigt, wie man strukturierte Dokument-Tags entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| id | int | Die Kennung des strukturierten Dokument-Tags. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt ein strukturiertes Dokument-Tag am angegebenen Index.

 **Examples:** 

Zeigt, wie man strukturierte Dokument-Tags entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Sammlung. |

