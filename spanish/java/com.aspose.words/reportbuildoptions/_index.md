---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words para Java"
description: "Especifica opciones que controlan el comportamiento de ReportingEngine al generar un informe en Java."
type: docs
weight: 570
url: /es/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Especifica opciones que controlan el comportamiento de [ReportingEngine](../../com.aspose.words/reportingengine/) al generar un informe.
## Campos

| Campo | Descripción |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Especifica que los miembros de objeto faltantes deben ser tratados como literales null por el motor. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Especifica que el motor debe insertar en línea los mensajes de error de sintaxis de plantilla en los documentos de salida. |
| [NONE](#NONE) | Especifica opciones predeterminadas. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Especifica que el motor debe eliminar los párrafos que quedan vacíos después de que las etiquetas de sintaxis de plantilla se eliminen o reemplacen por valores vacíos. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Especifica que el motor debe usar los valores de orientación de imagen EXIF \\u200b\\u200bimage para rotar adecuadamente las imágenes JPEG insertadas. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Especifica que el motor debe ignorar la sintaxis de plantilla en los resultados de los campos y actualizar los campos después de generar un informe. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Especifica que el motor debe visitar los nodos hijos de la sección (encabezados, pies de página, cuerpos) en un orden compatible con las versiones de Aspose.Words anteriores a la 21.9. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Especifica que los miembros de objeto faltantes deben ser tratados como literales nulos por el motor. Esta opción afecta solo al acceso a los miembros de instancia (es decir, no estáticos) y a los métodos de extensión. Si esta opción no está establecida, el motor lanza una excepción cuando encuentra un miembro de objeto faltante.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Especifica que el motor debe insertar en línea los mensajes de error de sintaxis de la plantilla en los documentos de salida. Si esta opción no está establecida, el motor lanza una excepción cuando encuentra un error de sintaxis.

### NONE {#NONE}
```
public static int NONE
```


Especifica opciones predeterminadas.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Especifica que el motor debe eliminar los párrafos que quedan vacíos después de que las etiquetas de sintaxis de plantilla se eliminen o reemplacen por valores vacíos.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Especifica que el motor debe usar los valores de orientación de imagen EXIF \\u200b\\u200bimage para rotar adecuadamente las imágenes JPEG insertadas.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Especifica que el motor debe ignorar la sintaxis de plantilla en los resultados de los campos y actualizar los campos después de generar un informe.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Especifica que el motor debe visitar los nodos hijos de la sección (encabezados, pies de página, cuerpos) en un orden compatible con las versiones de Aspose.Words anteriores a la 21.9.

 **Remarks:** 

Por defecto, el motor trata los encabezados y pies de página como si estuvieran vinculados a saltos de sección. Es decir, al visitar los nodos hijos de la sección, primero se visita el cuerpo y solo después se visitan los encabezados y pies de página. Esto coincide con el comportamiento de Microsoft Word al copiar/pegar o eliminar contenidos de varias secciones y produce resultados más correctos en la mayoría de los escenarios.

Antes de Aspose.Words 21.9, el motor utilizaba otro orden de visita: los nodos hijos de la sección se visitaban en el orden en que aparecen en el documento. Aplica este valor a [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) si se requiere compatibilidad con versiones anteriores de Aspose.Words.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
