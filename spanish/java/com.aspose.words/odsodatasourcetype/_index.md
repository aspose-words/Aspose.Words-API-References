---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de fuente de datos externa a la que se conectará como parte de la información de conexión ODSO en Java."
type: docs
weight: 488
url: /es/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Especifica el tipo de la fuente de datos externa a la que se conectará como parte de la información de conexión ODSO.

 **Remarks:** 

La especificación OOXML es muy vaga para este enumerado. Supongo que podría corresponder a la enumeración WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Campos

| Campo | Descripción |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Especifica que un documento dado ha sido conectado a una libreta de direcciones de contactos. |
| [DATABASE](#DATABASE) | Especifica que un documento dado ha sido conectado a una base de datos. |
| [DEFAULT](#DEFAULT) | Equivale a [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Especifica que un documento dado ha sido conectado a otro formato de documento soportado por la aplicación productora. |
| [DOCUMENT_2](#DOCUMENT-2) | Especifica que un documento dado ha sido conectado a otro formato de documento soportado por la aplicación productora. |
| [EMAIL](#EMAIL) | Especifica que un documento dado ha sido conectado a una aplicación de correo electrónico. |
| [LEGACY](#LEGACY) | Especifica que un documento dado ha sido conectado a un formato de documento heredado soportado por la aplicación productora. Posiblemente wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Especifica que un documento dado ha sido conectado a una fuente de datos que agrega otras fuentes de datos. |
| [NATIVE](#NATIVE) | Especifica que un documento dado ha sido conectado a otro formato de documento nativo de la aplicación productora. |
| [NONE](#NONE) | El tipo de la fuente de datos externa no está especificado. |
| [TEXT](#TEXT) | Especifica que un documento dado ha sido conectado a un archivo de texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Especifica que un documento dado ha sido conectado a una libreta de direcciones de contactos. Posiblemente wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Especifica que un documento dado ha sido conectado a una base de datos. Posiblemente wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equivale a [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Especifica que un documento dado ha sido conectado a otro formato de documento soportado por la aplicación productora. Posiblemente wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Especifica que un documento dado ha sido conectado a otro formato de documento soportado por la aplicación productora. Posiblemente wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Especifica que un documento dado ha sido conectado a una aplicación de correo electrónico. Posiblemente wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Especifica que un documento dado ha sido conectado a un formato de documento heredado soportado por la aplicación productora. Posiblemente wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Especifica que un documento dado ha sido conectado a una fuente de datos que agrega otras fuentes de datos.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Especifica que un documento dado ha sido conectado a otro formato de documento nativo de la aplicación productora. Posiblemente wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


El tipo de la fuente de datos externa no está especificado. Posiblemente wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Especifica que un documento dado ha sido conectado a un archivo de texto. Posiblemente wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
