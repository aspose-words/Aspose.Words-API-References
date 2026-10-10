---
title: "MailMergeDestination"
linktitle: "MailMergeDestination"
second_title: "Aspose.Words para Java"
description: "Especifica los posibles resultados que pueden generarse cuando se realiza una combinación de correspondencia en un documento en Java."
type: docs
weight: 441
url: /es/java/com.aspose.words/mailmergedestination/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDestination
```

Especifica los resultados posibles que pueden generarse cuando se realiza una combinación de correspondencia en un documento.
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | Equivale al valor [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination/\#NEW-DOCUMENT). |
| [EMAIL](#EMAIL) | Especifica que las aplicaciones anfitrionas conformes deben generar correos electrónicos utilizando los documentos que resultan de rellenar los campos dentro de un documento dado con datos de la fuente de datos externa especificada. |
| [FAX](#FAX) | Especifica que las aplicaciones anfitrionas conformes deben generar faxes utilizando los documentos que resultan de rellenar los campos dentro de un documento dado con datos de la fuente de datos externa especificada. |
| [NEW_DOCUMENT](#NEW-DOCUMENT) | Especifica que las aplicaciones anfitrionas conformes deben generar nuevos documentos rellenando los campos dentro de un documento dado con datos de la fuente de datos externa especificada. |
| [PRINTER](#PRINTER) | Especifica que las aplicaciones anfitrionas conformes deben imprimir los documentos que resultan de rellenar los campos dentro de un documento dado con datos externos de la fuente de datos externa especificada. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String mailMergeDestinationName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDestination)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDestination)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equivale al valor [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination/\#NEW-DOCUMENT).

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Especifica que las aplicaciones anfitrionas conformes deben generar correos electrónicos utilizando los documentos que resultan de rellenar los campos dentro de un documento dado con datos de la fuente de datos externa especificada.

### FAX {#FAX}
```
public static int FAX
```


Especifica que las aplicaciones anfitrionas conformes deben generar faxes utilizando los documentos que resultan de rellenar los campos dentro de un documento dado con datos de la fuente de datos externa especificada.

### NEW_DOCUMENT {#NEW-DOCUMENT}
```
public static int NEW_DOCUMENT
```


Especifica que las aplicaciones anfitrionas conformes deben generar nuevos documentos rellenando los campos dentro de un documento dado con datos de la fuente de datos externa especificada.

### PRINTER {#PRINTER}
```
public static int PRINTER
```


Especifica que las aplicaciones anfitrionas conformes deben imprimir los documentos que resultan de rellenar los campos dentro de un documento dado con datos externos de la fuente de datos externa especificada.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDestinationName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDestinationName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeDestinationName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDestination) {#getName-int}
```
public static String getName(int mailMergeDestination)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDestination) {#toString-int}
```
public static String toString(int mailMergeDestination)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
