---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words para Java"
description: "Representa los permisos de uso de incrustación de fuentes en Java."
type: docs
weight: 322
url: /es/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Representa los permisos de uso de incrustación de la fuente.

 **Examples:** 

Muestra cómo obtener información de derechos de licencia para fuentes incrustadas (FontInfo).

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [EDITABLE](#EDITABLE) | La fuente puede incrustarse y puede cargarse temporalmente en otros sistemas. |
| [INSTALLABLE](#INSTALLABLE) | La fuente puede incrustarse y puede instalarse permanentemente para su uso en sistemas remotos, o para uso por otros usuarios. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | La fuente puede incrustarse y puede cargarse temporalmente en otros sistemas con fines de visualización o impresión del documento. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | La fuente no debe modificarse, incrustarse ni intercambiarse de ninguna manera sin obtener primero el permiso explícito del propietario legal. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


La fuente puede incrustarse y puede cargarse temporalmente en otros sistemas.

 **Remarks:** 

Al igual que con la incrustación de Vista previa e Impresión, los documentos que contienen fuentes editables pueden abrirse para lectura. Además, se permite la edición, incluida la capacidad de formatear texto nuevo usando la fuente incrustada, y los cambios pueden guardarse.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


La fuente puede incrustarse y puede instalarse permanentemente para su uso en sistemas remotos, o para uso por otros usuarios.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


La fuente puede incrustarse y puede cargarse temporalmente en otros sistemas con fines de visualización o impresión del documento.

 **Remarks:** 

Los documentos que contienen fuentes de Vista previa e Impresión deben abrirse \\u201csolo lectura\\u201d; no se pueden aplicar ediciones al documento.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


La fuente no debe modificarse, incrustarse ni intercambiarse de ninguna manera sin obtener primero el permiso explícito del propietario legal.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontEmbeddingUsagePermissions) {#toString-int}
```
public static String toString(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
