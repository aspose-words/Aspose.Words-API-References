---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso a los valores de columna dentro de cada fila para un DataReader y es implementado por los proveedores de datos del .NET Framework que acceden a bases de datos relacionales en Java."
type: docs
weight: 35
url: /es/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Proporciona acceso a los valores de columna dentro de cada fila para un DataReader, y es implementado por los proveedores de datos del .NET Framework que acceden a bases de datos relacionales.
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int i)](#get-int) | Obtiene la columna ubicada en el índice especificado. |
| [getFieldCount()](#getFieldCount) | Obtiene el número de columnas en la fila actual. |
| [getFieldType(int i)](#getFieldType-int) | Obtiene la información de java.lang.Class correspondiente al tipo de java.lang.Object que se devolvería desde [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int). |
| [getName(int i)](#getName-int) | Obtiene el nombre del campo a buscar. |
| [getValue(int i)](#getValue-int) | Devuelve el valor del campo especificado. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Obtiene la columna ubicada en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| i | int | El índice basado en cero de la columna a obtener. |

**Returns:**
java.lang.Object - La columna ubicada en el índice especificado como un java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Obtiene el número de columnas en la fila actual.

**Returns:**
int - Cuando no está posicionado en un conjunto de registros válido, 0; de lo contrario, el número de columnas en el registro actual. El valor predeterminado es -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Obtiene la información de java.lang.Class correspondiente al tipo de java.lang.Object que se devolvería desde [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| i | int | El índice del campo a buscar. |

**Returns:**
java.lang.Class - La información de java.lang.Class correspondiente al tipo de java.lang.Object que se devolvería desde [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Obtiene el nombre del campo a buscar.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| i | int | El índice del campo a buscar. |

**Returns:**
java.lang.String - El nombre del campo o la cadena vacía (\"\"), si no hay valor que devolver.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Devuelve el valor del campo especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| i | int | El índice del campo a buscar. |

**Returns:**
java.lang.Object - El java.lang.Object que contendrá el valor del campo al devolverlo.
