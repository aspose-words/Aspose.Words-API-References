---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se debe mapear una columna en la fuente de datos externa a los campos de combinación predefinidos dentro del documento en Java."
type: docs
weight: 489
url: /es/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Especifica cómo se debe mapear una columna de la fuente de datos externa a los campos de combinación predefinidos dentro del documento.

Para obtener más información, visite el artículo de documentación [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Microsoft Word proporciona algunos nombres de campos de combinación predefinidos que permite insertar en un documento como MERGEFIELD o usar en los campos ADDRESSBLOCK o GREETINGLINE. La información especificada en [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) permite mapear una columna en la fuente de datos externa a un único campo de combinación predefinido.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Métodos

| Método | Descripción |
| --- | --- |
| [deepClone()](#deepClone) | Devuelve una clonación profunda de este objeto. |
| [getColumn()](#getColumn) | Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se debe mapear al nombre local de un campo MERGEFIELD específico. |
| [getMappedName()](#getMappedName) | Especifica el nombre del campo de combinación predefinido que se debe mapear al número de columna especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dentro de este mapeo de campo. |
| [getName()](#getName) | Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [getType()](#getType) | Especifica si un campo de combinación de correo dado ha sido mapeado a una columna en la fuente de datos externa dada o no. |
| [setColumn(int value)](#setColumn-int) | Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se debe mapear al nombre local de un campo MERGEFIELD específico. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Especifica el nombre del campo de combinación predefinido que se debe mapear al número de columna especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dentro de este mapeo de campo. |
| [setName(String value)](#setName-java.lang.String) | Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [setType(int value)](#setType-int) | Especifica si un campo de combinación de correo dado ha sido mapeado a una columna en la fuente de datos externa dada o no. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Devuelve una clonación profunda de este objeto.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se debe mapear al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0.

**Returns:**
int - El valor  int  correspondiente.
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Especifica el nombre del campo de combinación predefinido que se debe mapear al número de columna especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dentro de este mapeo de campo. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getName() {#getName}
```
public String getName()
```


Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getType() {#getType}
```
public int getType()
```


Especifica si un campo de combinación de correo dado ha sido mapeado a una columna en la fuente de datos externa dada o no. El valor predeterminado es [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Returns:**
int - El valor  int  correspondiente. El valor devuelto es una de las constantes de [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/).
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Especifica el índice basado en cero de la columna dentro de una fuente de datos externa que se debe mapear al nombre local de un campo MERGEFIELD específico. El valor predeterminado es 0.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Especifica el nombre del campo de combinación predefinido que se debe mapear al número de columna especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dentro de este mapeo de campo. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Especifica el nombre de la columna dentro de una fuente de datos externa para la columna cuyo índice está especificado por la propiedad [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Especifica si un campo de combinación de correo dado ha sido mapeado a una columna en la fuente de datos externa dada o no. El valor predeterminado es [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser una de las constantes de [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/). |

