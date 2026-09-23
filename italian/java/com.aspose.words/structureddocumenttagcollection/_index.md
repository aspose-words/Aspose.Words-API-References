---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words per Java"
description: "Una raccolta di istanze IStructuredDocumentTag che rappresentano i tag di documento strutturato nell'intervallo specificato in Java."
type: docs
weight: 638
url: /it/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

Una raccolta di istanze [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) che rappresentano i tag di documento strutturato nell'intervallo specificato.

Per saperne di più, visita l'articolo di documentazione [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Mostra come ottenere il tag di documento strutturato.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Restituisce il tag di documento strutturato all'indice specificato. |
| [getById(int id)](#getById-int) | Restituisce il tag di documento strutturato per identificatore. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Restituisce il primo tag di documento strutturato trovato nella raccolta con il tag specificato. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Restituisce il primo tag di documento strutturato trovato nella raccolta con il titolo specificato. |
| [getCount()](#getCount) | Restituisce il numero di tag di documento strutturato nella raccolta. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
| [remove(int id)](#remove-int) | Rimuove il tag di documento strutturato con l'identificatore specificato. |
| [removeAt(int index)](#removeAt-int) | Rimuove un tag di documento strutturato all'indice specificato. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Restituisce il tag di documento strutturato all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Un indice nella collezione. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Restituisce il tag di documento strutturato per identificatore.

 **Remarks:** 

Restituisce null se il tag di documento strutturato con l'identificatore specificato non può essere trovato.

 **Examples:** 

Mostra come ottenere il tag di documento strutturato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | int | L'identificatore del tag di documento strutturato. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Restituisce il primo tag di documento strutturato trovato nella raccolta con il tag specificato.

 **Remarks:** 

Restituisce null se il tag di documento strutturato con il tag specificato non può essere trovato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tag | java.lang.String | Il tag del tag del documento strutturato. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Restituisce il primo tag di documento strutturato trovato nella raccolta con il titolo specificato.

 **Remarks:** 

Restituisce null se il tag del documento strutturato con il titolo specificato non può essere trovato.

 **Examples:** 

Mostra come ottenere il tag di documento strutturato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| title | java.lang.String | Il titolo del tag del documento strutturato. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di tag di documento strutturato nella raccolta.

**Returns:**
int - Il numero di tag del documento strutturato nella collezione.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Rimuove il tag di documento strutturato con l'identificatore specificato.

 **Examples:** 

Mostra come rimuovere il tag di documento strutturato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | int | L'identificatore del tag di documento strutturato. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Rimuove un tag di documento strutturato all'indice specificato.

 **Examples:** 

Mostra come rimuovere il tag di documento strutturato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | Un indice nella collezione. |

