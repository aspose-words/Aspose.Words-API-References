---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words para Java"
description: "Especifica toda la información de combinación de correspondencia para un documento en Java."
type: docs
weight: 445
url: /es/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Especifica toda la información de mail merge para un documento.

Para obtener más información, visite el artículo de documentación [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Puede usar este objeto para especificar una fuente de datos de combinación de correspondencia para un documento y esta información (junto con los campos de datos disponibles) aparecerá en Microsoft Word cuando el usuario abra este documento. O puede usar este objeto para consultar la configuración de combinación de correspondencia que el usuario ha especificado en Microsoft Word para este documento.

Normalmente no necesita crear objetos de esta clase directamente porque la configuración de combinación de correspondencia de un documento siempre está disponible a través de la propiedad [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings).

Para detectar si este documento es un documento principal de combinación de correspondencia, verifique el valor de la propiedad [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int).

Para eliminar la configuración de combinación de correspondencia y la información de la fuente de datos de un documento, puede usar el método [clear()](../../com.aspose.words/mailmergesettings/\#clear). Aspose.Words no escribirá la configuración de combinación de correspondencia en un documento si la propiedad [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) está establecida en [MailMergeMainDocumentType.NOT\_A\_MERGE\_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) o la propiedad [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) está establecida en [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

La mejor manera de aprender a usar las propiedades de este objeto es crear un documento con la fuente de datos deseada manualmente en Microsoft Word y luego abrir ese documento usando Aspose.Words y examinar las propiedades de los objetos [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) y [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). Este es un buen enfoque si desea aprender a configurar programáticamente una fuente de datos, por ejemplo.

Aspose.Words conserva la información de combinación de correspondencia al cargar, guardar y convertir documentos entre diferentes formatos, pero no utiliza esta información al realizar su propia combinación de correspondencia usando el objeto [MailMerge](../../com.aspose.words/mailmerge/).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Métodos

| Método | Descripción |
| --- | --- |
| [clear()](#clear) | Borra la configuración de combinación de correspondencia de manera que, al guardar el documento, no se guarde ninguna configuración de combinación de correspondencia y el documento se convierta en un documento normal. |
| [deepClone()](#deepClone) | Devuelve una clonación profunda de este objeto. |
| [getActiveRecord()](#getActiveRecord) | Especifica el índice basado en uno del registro de la fuente de datos que se mostrará en Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName) | Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. |
| [getCheckErrors()](#getCheckErrors) | Especifica el tipo de informe de errores que Microsoft Word realizará al ejecutar una combinación de correspondencia. |
| [getConnectString()](#getConnectString) | Especifica la cadena de conexión utilizada para conectarse a una fuente de datos externa. |
| [getDataSource()](#getDataSource) | Especifica la ruta a la fuente de datos de combinación de correspondencia. |
| [getDataType()](#getDataType) | Especifica el tipo de la fuente de datos de combinación de correspondencia y el método de acceso a los datos. |
| [getDestination()](#getDestination) | Especifica cómo Microsoft Word producirá los resultados de una combinación de correspondencia. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Especifica cómo una aplicación que realiza la combinación de correspondencia debe manejar las líneas en blanco en los documentos combinados resultantes de la combinación de correspondencia. |
| [getHeaderSource()](#getHeaderSource) | Especifica la ruta al origen del encabezado de la combinación de correspondencia. |
| [getLinkToQuery()](#getLinkToQuery) | No estoy seguro de esto. |
| [getMailAsAttachment()](#getMailAsAttachment) | Especifica que los documentos producidos durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar del cuerpo del correo electrónico real. |
| [getMailSubject()](#getMailSubject) | Especifica el texto que aparecerá en la línea de asunto de los correos electrónicos o faxes producidos durante la combinación de correspondencia. |
| [getMainDocumentType()](#getMainDocumentType) | Especifica el tipo de documento principal de la combinación de correspondencia. |
| [getOdso()](#getOdso) | Obtiene el objeto que especifica la configuración del Office Data Source Object (ODSO). |
| [getQuery()](#getQuery) | Contiene la cadena Structured Query Language que se ejecutará contra la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. |
| [getViewMergedData()](#getViewMergedData) | Especifica que Microsoft Word mostrará los datos de la fuente de datos externa especificada donde se hayan insertado campos de combinación (p.ej. |
| [setActiveRecord(int value)](#setActiveRecord-int) | Especifica el índice basado en uno del registro de la fuente de datos que se mostrará en Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Especifica el tipo de informe de errores que Microsoft Word realizará al ejecutar una combinación de correspondencia. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Especifica la cadena de conexión utilizada para conectarse a una fuente de datos externa. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Especifica la ruta a la fuente de datos de combinación de correspondencia. |
| [setDataType(int value)](#setDataType-int) | Especifica el tipo de la fuente de datos de combinación de correspondencia y el método de acceso a los datos. |
| [setDestination(int value)](#setDestination-int) | Especifica cómo Microsoft Word producirá los resultados de una combinación de correspondencia. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Especifica cómo una aplicación que realiza la combinación de correspondencia debe manejar las líneas en blanco en los documentos combinados resultantes de la combinación de correspondencia. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Especifica la ruta al origen del encabezado de la combinación de correspondencia. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | No estoy seguro de esto. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Especifica que los documentos producidos durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar del cuerpo del correo electrónico real. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Especifica el texto que aparecerá en la línea de asunto de los correos electrónicos o faxes producidos durante la combinación de correspondencia. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Especifica el tipo de documento principal de la combinación de correspondencia. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Establece el objeto que especifica la configuración del Office Data Source Object (ODSO). |
| [setQuery(String value)](#setQuery-java.lang.String) | Contiene la cadena Structured Query Language que se ejecutará contra la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Especifica que Microsoft Word mostrará los datos de la fuente de datos externa especificada donde se hayan insertado campos de combinación (p.ej. |
### clear() {#clear}
```
public void clear()
```


Borra la configuración de combinación de correspondencia de manera que, al guardar el documento, no se guarde ninguna configuración de combinación de correspondencia y el documento se convierta en un documento normal.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Devuelve una clonación profunda de este objeto.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Especifica el índice basado en uno del registro de la fuente de datos que se mostrará en Microsoft Word. El valor predeterminado es 1.

**Returns:**
int - El valor  int  correspondiente.
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Especifica el tipo de informe de errores que Microsoft Word debe realizar al ejecutar una combinación de correspondencia. El valor predeterminado es [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/).
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Especifica la cadena de conexión utilizada para conectar a una fuente de datos externa. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Especifica la ruta a la fuente de datos de la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getDataType() {#getDataType}
```
public int getDataType()
```


Especifica el tipo de la fuente de datos de la combinación de correspondencia y el método de acceso a los datos. El valor predeterminado es [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes [MailMergeDataType](../../com.aspose.words/mailmergedatatype/).
### getDestination() {#getDestination}
```
public int getDestination()
```


Especifica cómo Microsoft Word producirá los resultados de una combinación de correspondencia. El valor predeterminado es [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes [MailMergeDestination](../../com.aspose.words/mailmergedestination/).
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Especifica cómo una aplicación que realiza la combinación de correspondencia debe manejar las líneas en blanco en los documentos combinados resultantes de la combinación de correspondencia. El valor predeterminado es false.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Especifica la ruta al origen del encabezado de la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


No estoy seguro de esto. La referencia de automatización de Microsoft Word sugiere que esto especifica que la consulta se ejecuta cada vez que el documento se abre en Microsoft Word. Pero la especificación OOXML sugiere que esto especifica que la consulta contiene una referencia a un archivo de consulta externo que contiene la consulta real. El valor predeterminado es false.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Especifica que los documentos producidos durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar del cuerpo del correo electrónico real. El valor predeterminado es false.

**Returns:**
boolean - El valor  boolean  correspondiente.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Especifica el texto que debe aparecer en la línea de asunto de los correos electrónicos o faxes generados durante la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Especifica el tipo de documento principal de la combinación de correspondencia. El valor predeterminado es [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

El documento principal es el documento que contiene información que es la misma para cada versión del documento combinado.

**Returns:**
int - El valor  int  correspondiente. El valor devuelto es una de las constantes de [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/).
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Obtiene el objeto que especifica la configuración del Office Data Source Object (ODSO).

 **Remarks:** 

Este objeto nunca es  null .

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Contiene la cadena Structured Query Language que se ejecutará contra la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Especifica que Microsoft Word debe mostrar los datos de la fuente de datos externa especificada donde se han insertado campos de combinación (p. ej., vista previa de los datos combinados). El valor predeterminado es  false .

**Returns:**
boolean - El valor  boolean  correspondiente.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Especifica el índice basado en uno del registro de la fuente de datos que se mostrará en Microsoft Word. El valor predeterminado es 1.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Especifica la columna dentro de la fuente de datos que contiene direcciones de correo electrónico. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Especifica el tipo de informe de errores que Microsoft Word debe realizar al ejecutar una combinación de correspondencia. El valor predeterminado es [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser una de las constantes de [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/). |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Especifica la cadena de conexión utilizada para conectar a una fuente de datos externa. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Especifica la ruta a la fuente de datos de la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Especifica el tipo de la fuente de datos de la combinación de correspondencia y el método de acceso a los datos. El valor predeterminado es [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser una de las constantes de [MailMergeDataType](../../com.aspose.words/mailmergedatatype/). |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Especifica cómo Microsoft Word producirá los resultados de una combinación de correspondencia. El valor predeterminado es [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser una de las constantes de [MailMergeDestination](../../com.aspose.words/mailmergedestination/). |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Especifica cómo una aplicación que realiza la combinación de correspondencia debe manejar las líneas en blanco en los documentos combinados resultantes de la combinación de correspondencia. El valor predeterminado es false.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Especifica la ruta al origen del encabezado de la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


No estoy seguro de esto. La referencia de automatización de Microsoft Word sugiere que esto especifica que la consulta se ejecuta cada vez que el documento se abre en Microsoft Word. Pero la especificación OOXML sugiere que esto especifica que la consulta contiene una referencia a un archivo de consulta externo que contiene la consulta real. El valor predeterminado es false.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Especifica que los documentos producidos durante una operación de combinación de correspondencia deben enviarse por correo electrónico como un archivo adjunto en lugar del cuerpo del correo electrónico real. El valor predeterminado es false.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Especifica el texto que debe aparecer en la línea de asunto de los correos electrónicos o faxes generados durante la combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Especifica el tipo de documento principal de la combinación de correspondencia. El valor predeterminado es [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

El documento principal es el documento que contiene información que es la misma para cada versión del documento combinado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser una de las constantes de [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/). |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Establece el objeto que especifica la configuración del Office Data Source Object (ODSO).

 **Remarks:** 

Este objeto nunca es  null .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | El objeto que especifica la configuración del Office Data Source Object (ODSO). |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Contiene la cadena Structured Query Language que se ejecutará contra la fuente de datos externa especificada para devolver el conjunto de registros que se importarán al documento cuando se realice la operación de combinación de correspondencia. El valor predeterminado es una cadena vacía.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Especifica que Microsoft Word debe mostrar los datos de la fuente de datos externa especificada donde se han insertado campos de combinación (p. ej., vista previa de los datos combinados). El valor predeterminado es  false .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

