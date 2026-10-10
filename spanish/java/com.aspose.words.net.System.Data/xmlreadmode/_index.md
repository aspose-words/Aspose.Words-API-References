---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo leer datos XML y un esquema relacional en un DataSet en Java."
type: docs
weight: 37
url: /es/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

Especifica cómo leer datos XML y un esquema relacional en un [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Predeterminado. |
| [DIFF_GRAM](#DIFF-GRAM) | Lee un DiffGram, aplicando los cambios del DiffGram al [DataSet](../../com.aspose.words.net.system.data/dataset/) y preservando los valores de [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState). |
| [FRAGMENT](#FRAGMENT) | Lee fragmentos XML, como los generados al ejecutar consultas FOR XML, contra una instancia de SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | Ignora cualquier esquema incrustado y lee los datos en el esquema existente del [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [INFER_SCHEMA](#INFER-SCHEMA) | Ignora cualquier esquema incrustado, infiere el esquema a partir de los datos y carga los datos. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Ignora cualquier esquema incrustado, infiere un esquema de tipo fuerte a partir de los datos y carga los datos. |
| [READ_SCHEMA](#READ-SCHEMA) | Lee cualquier esquema en línea y carga los datos. |
## Métodos

| Método | Descripción |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


Predeterminado.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


Lee un DiffGram, aplicando los cambios del DiffGram al [DataSet](../../com.aspose.words.net.system.data/dataset/) y preservando los valores de [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState).

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


Lee fragmentos XML, como los generados al ejecutar consultas FOR XML, contra una instancia de SQL Server. Cuando [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) está configurado en Fragment, el espacio de nombres predeterminado se lee como el esquema en línea.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


Ignora cualquier esquema en línea y lee los datos en el esquema existente del [DataSet](../../com.aspose.words.net.system.data/dataset/). Si algún dato no coincide con el esquema existente, se descarta (incluidos los datos de espacios de nombres diferentes definidos para el [DataSet](../../com.aspose.words.net.system.data/dataset/)). Si los datos son un DiffGram, IgnoreSchema tiene la misma funcionalidad que DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


Ignora cualquier esquema en línea, infiere el esquema a partir de los datos y carga los datos. Si el [DataSet](../../com.aspose.words.net.system.data/dataset/) ya contiene un esquema, el esquema actual se amplía añadiendo nuevas tablas o añadiendo columnas a tablas existentes. Se lanza una excepción si la tabla inferida ya existe pero con un espacio de nombres diferente, o si alguna de las columnas inferidas entra en conflicto con columnas existentes.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


Ignora cualquier esquema en línea, infiere un esquema fuertemente tipado a partir de los datos y carga los datos. Si el tipo no puede inferirse de los datos, se interpreta como datos de cadena. Si el [DataSet](../../com.aspose.words.net.system.data/dataset/) ya contiene un esquema, el esquema actual se amplía, ya sea añadiendo nuevas tablas o añadiendo columnas a tablas existentes. Se lanza una excepción si la tabla inferida ya existe pero con un espacio de nombres diferente, o si alguna de las columnas inferidas entra en conflicto con columnas existentes.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


Lee cualquier esquema en línea y carga los datos. Si el [DataSet](../../com.aspose.words.net.system.data/dataset/) ya contiene un esquema, se pueden añadir nuevas tablas al esquema, pero se lanza una excepción si alguna tabla del esquema en línea ya existe en el [DataSet](../../com.aspose.words.net.system.data/dataset/).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
