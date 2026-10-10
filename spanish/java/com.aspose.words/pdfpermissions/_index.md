---
title: "PdfPermissions"
linktitle: "PdfPermissions"
second_title: "Aspose.Words para Java"
description: "Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado en Java."
type: docs
weight: 541
url: /es/java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado.

 **Examples:** 

Muestra cómo establecer permisos en un documento PDF guardado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | Permite todas las operaciones en el documento PDF. |
| [CONTENT_COPY](#CONTENT-COPY) | Copiar o extraer de otro modo texto y gráficos del documento mediante operaciones distintas a las controladas por [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Extraer texto y gráficos (para apoyar la accesibilidad a usuarios con discapacidades o para otros propósitos). |
| [DISALLOW_ALL](#DISALLOW-ALL) | No permite ninguna operación en el documento PDF. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Ensambla el documento (inserta, rota o elimina páginas y crea elementos de esquema del documento o imágenes en miniatura), incluso si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) está desactivado. |
| [FILL_IN](#FILL-IN) | Rellena los campos de formulario interactivo existentes (incluidos los campos de firma), incluso si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) está desactivado. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Imprime el documento a una representación a partir de la cual se pueda generar una copia digital fiel del contenido PDF, basada en un algoritmo dependiente de la implementación. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Agregar o modificar anotaciones de texto, rellenar campos de formulario interactivo y, si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) también está activado, crear o modificar campos de formulario interactivo (incluidos los campos de firma). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Modificar el contenido del documento mediante operaciones distintas a las controladas por [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) y [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) | Imprime el documento (posiblemente no al nivel de mayor calidad, dependiendo de si [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) también está activado). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set) |  |
| [getName(int pdfPermissions)](#getName-int) |  |
| [getNames(int pdfPermissions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPermissions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Permite todas las operaciones en el documento PDF.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Copiar o extraer de otro modo texto y gráficos del documento mediante operaciones distintas a las controladas por [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Extraer texto y gráficos (para apoyar la accesibilidad a usuarios con discapacidades o para otros propósitos).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


No permite ninguna operación en el documento PDF. Este es el valor predeterminado.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Ensambla el documento (inserta, rota o elimina páginas y crea elementos de esquema del documento o imágenes en miniatura), incluso si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) está desactivado.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Rellena los campos de formulario interactivo existentes (incluidos los campos de firma), incluso si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) está desactivado.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Imprime el documento a una representación a partir de la cual se pueda generar una copia digital fiel del contenido PDF, basada en un algoritmo dependiente de la implementación. Cuando esta bandera está desactivada (y [PRINTING](../../com.aspose.words/pdfpermissions/\#PRINTING) está activado), la impresión se limitará a una representación de bajo nivel de la apariencia, posiblemente de calidad degradada.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Agregar o modificar anotaciones de texto, rellenar campos de formulario interactivo y, si [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions/\#MODIFY-CONTENTS) también está activado, crear o modificar campos de formulario interactivo (incluidos los campos de firma).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Modificar el contenido del documento mediante operaciones distintas a las controladas por [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions/\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions/\#FILL-IN) y [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions/\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Imprime el documento (posiblemente no al nivel de mayor calidad, dependiendo de si [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions/\#HIGH-RESOLUTION-PRINTING) también está activado).

### length {#length}
```
public static int length
```


### fromName(String pdfPermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getName(int pdfPermissions) {#getName-int}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPermissions) {#toString-int}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
