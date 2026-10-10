---
title: "StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words pour Java"
description: "Une collection d'instances IStructuredDocumentTag qui représentent les balises de document structuré dans la plage spécifiée en Java."
type: docs
weight: 638
url: /fr/java/com.aspose.words/structureddocumenttagcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

Une collection d'instances [IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) qui représentent les balises de document structuré dans la plage spécifiée.

Pour en savoir plus, consultez l'article de documentation [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Montre comment obtenir une balise de document structuré.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Renvoie la balise de document structuré à l'index spécifié. |
| [getById(int id)](#getById-int) | Renvoie la balise de document structuré par identifiant. |
| [getByTag(String tag)](#getByTag-java.lang.String) | Renvoie la première balise de document structuré rencontrée dans la collection avec la balise spécifiée. |
| [getByTitle(String title)](#getByTitle-java.lang.String) | Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié. |
| [getCount()](#getCount) | Renvoie le nombre de balises de document structuré dans la collection. |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
| [remove(int id)](#remove-int) | Supprime la balise de document structuré avec l'identifiant spécifié. |
| [removeAt(int index)](#removeAt-int) | Supprime une balise de document structuré à l'index spécifié. |
### get(int index) {#get-int}
```
public IStructuredDocumentTag get(int index)
```


Renvoie la balise de document structuré à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/) - The structured document tag at the specified index.
### getById(int id) {#getById-int}
```
public IStructuredDocumentTag getById(int id)
```


Renvoie la balise de document structuré par identifiant.

 **Remarks:** 

Renvoie null si la balise de document structuré avec l'identifiant spécifié ne peut pas être trouvée.

 **Examples:** 

Montre comment obtenir une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| id | int | L'identifiant de la balise de document structuré. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTag(String tag) {#getByTag-java.lang.String}
```
public IStructuredDocumentTag getByTag(String tag)
```


Renvoie la première balise de document structuré rencontrée dans la collection avec la balise spécifiée.

 **Remarks:** 

Renvoie null si la balise de document structuré avec la balise spécifiée ne peut pas être trouvée.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| balise | java.lang.String | La balise du tag de document structuré. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getByTitle(String title) {#getByTitle-java.lang.String}
```
public IStructuredDocumentTag getByTitle(String title)
```


Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié.

 **Remarks:** 

Renvoie null si le tag de document structuré avec le titre spécifié ne peut pas être trouvé.

 **Examples:** 

Montre comment obtenir une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| titre | java.lang.String | Le titre du tag de document structuré. |

**Returns:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
### getCount() {#getCount}
```
public int getCount()
```


Renvoie le nombre de balises de document structuré dans la collection.

**Returns:**
int - Le nombre de tags de document structuré dans la collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur.

**Returns:**
java.util.Iterator
### remove(int id) {#remove-int}
```
public void remove(int id)
```


Supprime la balise de document structuré avec l'identifiant spécifié.

 **Examples:** 

Montre comment supprimer une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| id | int | L'identifiant de la balise de document structuré. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Supprime une balise de document structuré à l'index spécifié.

 **Examples:** 

Montre comment supprimer une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |

