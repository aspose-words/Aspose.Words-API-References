---
title: "CustomPartCollection"
linktitle: "CustomPartCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de objetos CustomPart en Java."
type: docs
weight: 142
url: /es/java/com.aspose.words/custompartcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomPartCollection implements Iterable
```

Representa una colección de objetos [CustomPart](../../com.aspose.words/custompart/).

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Normalmente no necesita crear instancias de esta clase. Accede a las partes personalizadas relacionadas con el paquete OOXML a través de la propiedad [Document.getPackageCustomParts()](../../com.aspose.words/document/\#getPackageCustomParts) / [Document.setPackageCustomParts(com.aspose.words.CustomPartCollection)](../../com.aspose.words/document/\#setPackageCustomParts-com.aspose.words.CustomPartCollection).

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Métodos

| Método | Descripción |
| --- | --- |
| [add(CustomPart part)](#add-com.aspose.words.CustomPart) | Añade un elemento a la colección. |
| [clear()](#clear) | Elimina todos los elementos de la colección. |
| [deepClone()](#deepClone) | Crea una copia profunda de esta colección y sus elementos. |
| [get(int index)](#get-int) | Obtiene un elemento en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina un elemento en el índice especificado. |
| [set(int index, CustomPart value)](#set-int-com.aspose.words.CustomPart) | Establece un elemento en el índice especificado. |
### add(CustomPart part) {#add-com.aspose.words.CustomPart}
```
public void add(CustomPart part)
```


Añade un elemento a la colección.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| part | [CustomPart](../../com.aspose.words/custompart/) | El elemento a añadir. |

### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de la colección.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

### deepClone() {#deepClone}
```
public CustomPartCollection deepClone()
```


Crea una copia profunda de esta colección y sus elementos.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
[CustomPartCollection](../../com.aspose.words/custompartcollection/)
### get(int index) {#get-int}
```
public CustomPart get(int index)
```


Obtiene un elemento en el índice especificado.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero del elemento. |

**Returns:**
[CustomPart](../../com.aspose.words/custompart/) - An item at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
int - El número de elementos contenidos en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina un elemento en el índice especificado.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero. |

### set(int index, CustomPart value) {#set-int-com.aspose.words.CustomPart}
```
public void set(int index, CustomPart value)
```


Establece un elemento en el índice especificado.

 **Examples:** 

Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero del elemento. |
| value | [CustomPart](../../com.aspose.words/custompart/) | Un elemento en el índice especificado. |

