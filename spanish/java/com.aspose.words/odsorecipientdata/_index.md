---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words para Java"
description: "Representa información sobre un único registro dentro de una fuente de datos externa que debe excluirse de la combinación de correspondencia en Java."
type: docs
weight: 492
url: /es/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Representa información sobre un registro único dentro de una fuente de datos externa que debe excluirse de la combinación de correspondencia.

Para obtener más información, visite el artículo de documentación [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Si un registro debe fusionarse en un documento combinado, no se necesita información sobre ese registro. Sin embargo, si un registro dado no debe fusionarse en un documento combinado, entonces el valor de la clave única para ese registro debe almacenarse en la propiedad [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) de este objeto para indicar esta exclusión.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Métodos

| Método | Descripción |
| --- | --- |
| [deepClone()](#deepClone) | Devuelve una clonación profunda de este objeto. |
| [getActive()](#getActive) | Especifica si el registro de la fuente de datos debe importarse a un documento cuando se realiza la combinación de correspondencia. |
| [getColumn()](#getColumn) | Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. |
| [getHash()](#getHash) | Representa el código hash de este registro. |
| [getUniqueTag()](#getUniqueTag) | Especifica el contenido de un registro dado en la columna que contiene datos únicos. |
| [setActive(boolean value)](#setActive-boolean) | Especifica si el registro de la fuente de datos debe importarse a un documento cuando se realiza la combinación de correspondencia. |
| [setColumn(int value)](#setColumn-int) | Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. |
| [setHash(int value)](#setHash-int) | Representa el código hash de este registro. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Especifica el contenido de un registro dado en la columna que contiene datos únicos. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Devuelve una clonación profunda de este objeto.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Especifica si el registro de la fuente de datos debe importarse a un documento cuando se realiza la combinación de correspondencia. El valor predeterminado es  true .

**Returns:**
boolean - El valor  boolean  correspondiente.
### getColumn() {#getColumn}
```
public int getColumn()
```


Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0.

**Returns:**
int - El valor  int  correspondiente.
### getHash() {#getHash}
```
public int getHash()
```


Representa el código hash de este registro. A veces Microsoft Word usa [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) de un registro completo en lugar de un valor [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). El valor predeterminado es 0.

**Returns:**
int - El valor  int  correspondiente.
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Especifica el contenido de un registro dado en la columna que contiene datos únicos. El valor predeterminado es  null .

**Returns:**
byte[] - El valor byte[] correspondiente.
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Especifica si el registro de la fuente de datos debe importarse a un documento cuando se realiza la combinación de correspondencia. El valor predeterminado es  true .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Especifica la columna dentro de la fuente de datos que contiene datos únicos para el registro actual. El valor predeterminado es 0.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Representa el código hash de este registro. A veces Microsoft Word usa [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) de un registro completo en lugar de un valor [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). El valor predeterminado es 0.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Especifica el contenido de un registro dado en la columna que contiene datos únicos. El valor predeterminado es  null .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | byte[] | El valor byte[] correspondiente. |

