---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words para Java"
description: "Representa una parte de contenido arbitrario personalizada que no está definida por la norma ISO/IEC 29500 en Java."
type: docs
weight: 141
url: /es/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Representa una parte personalizada (contenido arbitrario) que no está definida por la norma ISO/IEC 29500.

Para obtener más información, visite el artículo de documentación [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Esta clase representa una parte OOXML que es el objetivo de una "relación desconocida". Todas las relaciones que no están definidas dentro de ISO/IEC 29500 se consideran "relaciones desconocidas". Las relaciones desconocidas están permitidas dentro de un documento Office Open XML siempre que cumplan con las directrices de marcado de relaciones.

Microsoft Word conserva las partes personalizadas durante los ciclos de apertura/guardado. Se puede encontrar información adicional aquí http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words también mantiene las partes personalizadas en los procesos de lectura/escritura y, además, permite acceder programáticamente a dichas partes mediante los objetos [CustomPart](../../com.aspose.words/custompart/) y [CustomPartCollection](../../com.aspose.words/custompartcollection/).

No confunda las partes personalizadas con Custom XML Data. Utilice [CustomXmlPart](../../com.aspose.words/customxmlpart/) si necesita acceder a Custom XML Data.

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
| [deepClone()](#deepClone) | Crea una copia "suficientemente profunda" del objeto. |
| [getContentType()](#getContentType) | Especifica el tipo de contenido de esta parte personalizada. |
| [getData()](#getData) | Contiene los datos de esta parte personalizada. |
| [getName()](#getName) | Obtiene el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino. |
| [getRelationshipType()](#getRelationshipType) | Obtiene el tipo de relación desde la parte padre a esta parte personalizada. |
| [isExternal()](#isExternal) | Falso si esta parte personalizada se almacena dentro del paquete OOXML. |
| [isExternal(boolean value)](#isExternal-boolean) | Falso si esta parte personalizada se almacena dentro del paquete OOXML. |
| [setContentType(String value)](#setContentType-java.lang.String) | Especifica el tipo de contenido de esta parte personalizada. |
| [setData(byte[] value)](#setData-byte) | Contiene los datos de esta parte personalizada. |
| [setName(String value)](#setName-java.lang.String) | Establece el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | Establece el tipo de relación desde la parte padre a esta parte personalizada. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


Crea una copia "suficientemente profunda" del objeto. No duplica los bytes del valor de [getData()](../../com.aspose.words/custompart/\#getData) / [setData(byte[])](../../com.aspose.words/custompart/\#setData-byte).

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
[CustomPart](../../com.aspose.words/custompart/)
### getContentType() {#getContentType}
```
public String getContentType()
```


Especifica el tipo de contenido de esta parte personalizada.

 **Remarks:** 

Esta propiedad es aplicable solo cuando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) es false.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

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
java.lang.String - El valor java.lang.String correspondiente.
### getData() {#getData}
```
public byte[] getData()
```


Contiene los datos de esta parte personalizada.

 **Remarks:** 

Esta propiedad es aplicable solo cuando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) es false.

El valor predeterminado es una matriz de bytes vacía. El valor no puede ser nulo.

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
byte[] - El valor byte[] correspondiente.
### getName() {#getName}
```
public String getName()
```


Obtiene el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino.

 **Remarks:** 

Si el objetivo de la relación es interno, entonces esta propiedad es el nombre absoluto de la parte dentro del paquete. Si el objetivo de la relación es externo, entonces esta propiedad es la URL de destino.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

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
java.lang.String - El nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


Obtiene el tipo de relación desde la parte padre a esta parte personalizada.

 **Remarks:** 

El tipo de relación para una parte personalizada debe ser "unknown", por ejemplo un tipo de relación personalizada, no uno de los tipos de relación definidos dentro de ISO/IEC 29500.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

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
java.lang.String - El tipo de relación desde la parte padre a esta parte personalizada.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


Falso si esta parte personalizada se almacena dentro del paquete OOXML. Verdadero si esta parte personalizada es un objetivo externo.

 **Remarks:** 

El valor predeterminado es  false .

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
boolean - El valor  boolean  correspondiente.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


Falso si esta parte personalizada se almacena dentro del paquete OOXML. Verdadero si esta parte personalizada es un objetivo externo.

 **Remarks:** 

El valor predeterminado es  false .

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
| valor | boolean | El valor  boolean  correspondiente. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Especifica el tipo de contenido de esta parte personalizada.

 **Remarks:** 

Esta propiedad es aplicable solo cuando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) es false.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

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
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Contiene los datos de esta parte personalizada.

 **Remarks:** 

Esta propiedad es aplicable solo cuando [isExternal()](../../com.aspose.words/custompart/\#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/\#isExternal-boolean) es false.

El valor predeterminado es una matriz de bytes vacía. El valor no puede ser nulo.

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
| valor | byte[] | El valor byte[] correspondiente. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Establece el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino.

 **Remarks:** 

Si el objetivo de la relación es interno, entonces esta propiedad es el nombre absoluto de la parte dentro del paquete. Si el objetivo de la relación es externo, entonces esta propiedad es la URL de destino.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

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
| valor | java.lang.String | El nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


Establece el tipo de relación desde la parte padre a esta parte personalizada.

 **Remarks:** 

El tipo de relación para una parte personalizada debe ser "unknown", por ejemplo un tipo de relación personalizada, no uno de los tipos de relación definidos dentro de ISO/IEC 29500.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

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
| valor | java.lang.String | El tipo de relación desde la parte padre a esta parte personalizada. |

