---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words para Java"
description: "Enumera diferentes formas de presentar el documento en el navegador del cliente en Java."
type: docs
weight: 126
url: /es/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Enumera diferentes formas de presentar el documento en el navegador del cliente.

 **Remarks:** 

Tenga en cuenta que el comportamiento real en el navegador del cliente podría verse afectado por la configuración de seguridad del navegador.

 **Examples:** 

Muestra cómo realizar una combinación de correspondencia y luego guardar el documento en el navegador del cliente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Envía el documento al navegador y presenta una opción para guardar el documento en el disco o abrirlo en la aplicación asociada con la extensión del documento. |
| [INLINE](#INLINE) | Envía el documento al navegador y presenta una opción para guardar el documento en el disco o abrirlo dentro del navegador. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Envía el documento al navegador y presenta una opción para guardar el documento en el disco o abrirlo en la aplicación asociada con la extensión del documento.

### INLINE {#INLINE}
```
public static int INLINE
```


Envía el documento al navegador y presenta una opción para guardar el documento en el disco o abrirlo dentro del navegador.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
