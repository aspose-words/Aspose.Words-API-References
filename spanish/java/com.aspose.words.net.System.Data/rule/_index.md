---
title: "Regla"
linktitle: "Regla"
second_title: "Aspose.Words para Java"
description: "Indica la acción que ocurre cuando se aplica una ForeignKeyConstraint en Java."
type: docs
weight: 36
url: /es/java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

Indica la acción que ocurre cuando se aplica una [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
## Campos

| Campo | Descripción |
| --- | --- |
| [CASCADE](#CASCADE) | Eliminar o actualizar filas relacionadas. |
| [NONE](#NONE) | No se realiza ninguna acción sobre las filas relacionadas. |
| [SET_DEFAULT](#SET-DEFAULT) | Establece valores en filas relacionadas al valor contenido en la propiedad [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object). |
| [SET_NULL](#SET-NULL) | Establece valores en filas relacionadas a DBNull. |
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
### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


Eliminar o actualizar filas relacionadas. Este es el valor predeterminado.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


No se realiza ninguna acción sobre las filas relacionadas.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


Establece valores en filas relacionadas al valor contenido en la propiedad [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object).

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


Establece valores en filas relacionadas a DBNull.

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
public static System.Data.Rule valueOf(String name)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String |  |

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/)
### values() {#values}
```
public static System.Data.Rule[] values()
```




**Returns:**
com.aspose.words.net.System.Data.Rule[]
