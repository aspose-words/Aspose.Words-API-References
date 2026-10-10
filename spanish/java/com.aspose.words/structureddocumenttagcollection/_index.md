---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words para Java"
description: "Una colección de instancias de IStructuredDocumentTag que representan las etiquetas de documento estructurado en el rango especificado en Java."
type: docs
weight: 638
url: /es/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

Una colección de instancias de [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) que representan las etiquetas de documento estructurado en el rango especificado.

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Muestra cómo obtener la etiqueta de documento estructurado.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Devuelve la etiqueta de documento estructurado en el índice especificado. |
| [getById(int id)](#getById-int) | Devuelve la etiqueta de documento estructurado por identificador. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Devuelve la primera etiqueta de documento estructurado encontrada en la colección con la etiqueta especificada. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado. |
| [getCount()](#getCount) | Devuelve el número de etiquetas de documento estructurado en la colección. |
| [iterator()](#iterator) | Devuelve un objeto enumerador. |
| [remove(int id)](#remove-int) | Elimina la etiqueta de documento estructurado con el identificador especificado. |
| [removeAt(int index)](#removeAt-int) | Elimina una etiqueta de documento estructurado en el índice especificado. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Devuelve la etiqueta de documento estructurado en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Un índice en la colección. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Devuelve la etiqueta de documento estructurado por identificador.

 **Remarks:** 

Devuelve null si no se puede encontrar la etiqueta de documento estructurado con el identificador especificado.

 **Examples:** 

Muestra cómo obtener la etiqueta de documento estructurado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| id | int | El identificador de la etiqueta de documento estructurado. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Devuelve la primera etiqueta de documento estructurado encontrada en la colección con la etiqueta especificada.

 **Remarks:** 

Devuelve null si no se puede encontrar la etiqueta de documento estructurado con la etiqueta especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| etiqueta | java.lang.String | La etiqueta del tag de documento estructurado. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado.

 **Remarks:** 

Devuelve null si no se puede encontrar el tag de documento estructurado con el título especificado.

 **Examples:** 

Muestra cómo obtener la etiqueta de documento estructurado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| título | java.lang.String | El título del tag de documento estructurado. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Devuelve el número de etiquetas de documento estructurado en la colección.

**Returns:**
int - El número de tags de documento estructurado en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto enumerador.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Elimina la etiqueta de documento estructurado con el identificador especificado.

 **Examples:** 

Muestra cómo eliminar una etiqueta de documento estructurado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| id | int | El identificador de la etiqueta de documento estructurado. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina una etiqueta de documento estructurado en el índice especificado.

 **Examples:** 

Muestra cómo eliminar una etiqueta de documento estructurado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Un índice en la colección. |

