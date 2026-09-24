---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words para Java"
description: "Especifica la configuración del Office Data Source Object ODSO para una fuente de datos de combinación de correspondencia en Java."
type: docs
weight: 487
url: /es/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Especifica la configuración del Office Data Source Object (ODSO) para una fuente de datos de combinación de correspondencia.

Para obtener más información, visite el artículo de documentación [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

ODSO parece ser la forma "nueva" que las versiones más recientes de Microsoft Word prefieren usar al especificar ciertos tipos de fuentes de datos para un documento de combinación de correspondencia. ODSO probablemente apareció por primera vez en Microsoft Word 2000.

El uso de ODSO está pobremente documentado y la mejor manera de aprender a usar las propiedades de este objeto es crear un documento con una fuente de datos deseada manualmente en Microsoft Word y luego abrir ese documento usando Aspose.Words y examinar las propiedades de los objetos [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) y [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). Este es un buen enfoque si deseas aprender a configurar programáticamente una fuente de datos, por ejemplo.

No necesitas normalmente crear objetos de esta clase directamente porque la configuración ODSO siempre está disponible a través de la propiedad [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Métodos

| Método | Descripción |
| --- | --- |
| [deepClone()](#deepClone) | Devuelve una clonación profunda de este objeto. |
| [getColumnDelimiter()](#getColumnDelimiter) | Especifica el carácter que se interpretará como delimitador de columnas utilizado para separar columnas dentro de fuentes de datos externas. |
| [getDataSource()](#getDataSource) | Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. |
| [getDataSourceType()](#getDataSourceType) | Especifica el tipo de la fuente de datos externa que se conectará como parte de la información de conexión ODSO para esta combinación de correspondencia. |
| [getFieldMapDatas()](#getFieldMapDatas) | Obtiene una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campos de combinación predefinidos en el documento. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Especifica que una aplicación anfitriona debe tratar la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. |
| [getRecipientDatas()](#getRecipientDatas) | Obtiene una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. |
| [getTableName()](#getTableName) | Especifica el conjunto particular de datos al que una fuente debe conectarse dentro de una fuente de datos externa. |
| [getUdlConnectString()](#getUdlConnectString) | Especifica la cadena de conexión Universal Data Link (UDL) utilizada para conectarse a una fuente de datos externa. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Especifica el carácter que se interpretará como delimitador de columnas utilizado para separar columnas dentro de fuentes de datos externas. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Especifica el tipo de la fuente de datos externa que se conectará como parte de la información de conexión ODSO para esta combinación de correspondencia. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Establece una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campos de combinación predefinidos en el documento. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Especifica que una aplicación anfitriona debe tratar la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Establece una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. |
| [setTableName(String value)](#setTableName-java.lang.String) | Especifica el conjunto particular de datos al que una fuente debe conectarse dentro de una fuente de datos externa. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Especifica la cadena de conexión Universal Data Link (UDL) utilizada para conectarse a una fuente de datos externa. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Devuelve una clonación profunda de este objeto.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Especifica el carácter que se interpretará como delimitador de columnas utilizado para separar columnas dentro de fuentes de datos externas. El valor predeterminado es 0, lo que significa que no hay delimitador de columnas definido.

 **Remarks:** 

RK nunca he visto esto en uso.

**Returns:**
`char` - El valor `char` correspondiente.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Especifica el tipo de la fuente de datos externa que se conectará como parte de la información de conexión ODSO para esta combinación de correspondencia. El valor predeterminado es [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Esta configuración es simplemente una sugerencia del tipo de fuente de datos que se está utilizando para esta combinación de correspondencia.

**Returns:**
`int` - El valor `int` correspondiente. El valor devuelto es una de las constantes de [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/).
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Obtiene una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campos de combinación predefinidos en el documento. Este objeto nunca es null.

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Especifica que una aplicación anfitriona debe tratar la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. El valor predeterminado es false.

 **Remarks:** 

RK nunca he visto esto en uso.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Obtiene una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nunca es null.

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Especifica el conjunto particular de datos al que una fuente debe conectarse dentro de una fuente de datos externa. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Especifica la cadena de conexión Universal Data Link (UDL) utilizada para conectar a una fuente de datos externa. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Especifica el carácter que se interpretará como delimitador de columnas utilizado para separar columnas dentro de fuentes de datos externas. El valor predeterminado es 0, lo que significa que no hay delimitador de columnas definido.

 **Remarks:** 

RK nunca he visto esto en uso.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | char | El valor correspondiente  char  . |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Especifica la ubicación de la fuente de datos externa que se conectará a un documento para realizar la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Especifica el tipo de la fuente de datos externa que se conectará como parte de la información de conexión ODSO para esta combinación de correspondencia. El valor predeterminado es [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Esta configuración es simplemente una sugerencia del tipo de fuente de datos que se está utilizando para esta combinación de correspondencia.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor correspondiente  int  . El valor debe ser uno de los constantes de [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/). |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Establece una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campo de combinación predefinidos en el documento. Este objeto nunca es  null .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | Una colección de objetos que especifican cómo se asignan las columnas de la fuente de datos externa a los nombres de campo de combinación predefinidos en el documento. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Especifica que una aplicación anfitriona debe tratar la primera fila de datos en la fuente de datos externa especificada como una fila de encabezado que contiene los nombres de cada columna en la fuente de datos. El valor predeterminado es false.

 **Remarks:** 

RK nunca he visto esto en uso.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Establece una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. Este objeto nunca es  null .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | Una colección de objetos que especifican la inclusión/exclusión de registros individuales en la combinación de correspondencia. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Especifica el conjunto particular de datos al que una fuente debe conectarse dentro de una fuente de datos externa. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Especifica la cadena de conexión Universal Data Link (UDL) utilizada para conectar a una fuente de datos externa. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

