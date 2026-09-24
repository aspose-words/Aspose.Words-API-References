---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words para Java"
description: "Representa el esquema de una columna en un DataTable en Java."
type: docs
weight: 14
url: /es/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Representa el esquema de una columna en un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DataColumn()](#DataColumn) | Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) como tipo cadena. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), como tipo cadena, usando el nombre de columna especificado. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Inicializa una nueva instancia de la clase @\{link DataColumn\} usando el nombre de columna especificado y la tabla a la que pertenece. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) usando el nombre de columna especificado y el tipo de datos. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) usando el nombre de columna especificado, el tipo de datos y la tabla de datos a la que pertenece. |
## Métodos

| Método | Descripción |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Obtiene un valor que indica si se permiten valores nulos en esta columna para las filas que pertenecen a la tabla. |
| [getAutoIncrement()](#getAutoIncrement) | Obtiene un valor que indica si la columna incrementa automáticamente el valor de la columna para las nuevas filas añadidas a la tabla. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Obtiene el valor inicial para una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Obtiene el incremento utilizado por una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true. |
| [getCaption()](#getCaption) | Obtiene el título de la columna. |
| [getColumnMapping()](#getColumnMapping) | Obtiene el [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la columna. |
| [getColumnName()](#getColumnName) | Obtiene el nombre de la columna en la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getDataType()](#getDataType) | Obtiene el tipo de datos almacenados en la columna. |
| [getDefaultValue()](#getDefaultValue) | Obtiene el valor predeterminado para la columna al crear nuevas filas. |
| [getExpression()](#getExpression) | Obtiene la expresión utilizada para filtrar filas, calcular los valores en una columna o crear una columna agregada. |
| [getMaxLength()](#getMaxLength) | Obtiene la longitud máxima de una columna de texto. |
| [getNamespace()](#getNamespace) | Obtiene el espacio de nombres del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [getOrdinal()](#getOrdinal) | Obtiene la posición de la columna en la colección [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getPrefix()](#getPrefix) | Obtiene un prefijo XML que hace alias al espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getReadOnly()](#getReadOnly) | Obtiene un valor que indica si la columna permite cambios tan pronto como se ha añadido una fila a la tabla. |
| [getTable()](#getTable) | Obtiene el [DataTable](../../com.aspose.words.net.system.data/datatable/) al que pertenece la columna. |
| [getUnique()](#getUnique) | Obtiene un valor que indica si los valores en cada fila de la columna deben ser únicos. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Establece un valor que indica si se permiten valores nulos en esta columna para las filas que pertenecen a la tabla. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Establece un valor que indica si la columna incrementa automáticamente el valor de la columna para las nuevas filas añadidas a la tabla. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Establece el valor inicial para una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Establece el incremento utilizado por una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true. |
| [setCaption(String value)](#setCaption-java.lang.String) | Establece el título de la columna. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Establece el [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la columna. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Establece el nombre de la columna en la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Establece el tipo de datos almacenados en la columna. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Establece el valor predeterminado para la columna al crear nuevas filas. |
| [setMaxLength(int value)](#setMaxLength-int) | Establece la longitud máxima de una columna de texto. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Establece el espacio de nombres del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [setOrdinal(int ordinal)](#setOrdinal-int) | Cambia el ordinal o la posición del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) al ordinal o posición especificados. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | Establece un prefijo XML que actúa como alias del espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Establece un valor que indica si la columna permite cambios tan pronto como se ha añadido una fila a la tabla. |
| [setUnique(boolean value)](#setUnique-boolean) | Establece un valor que indica si los valores en cada fila de la columna deben ser únicos. |
| [toString()](#toString) | Obtiene el [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) de la columna, si existe. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) como tipo cadena.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), como tipo cadena, usando el nombre de columna especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | Una cadena que representa el nombre de la columna a crear. Si se establece en null o una cadena vacía (""), se especificará un nombre predeterminado al agregarla a la colección de columnas. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Inicializa una nueva instancia de la clase @\{link DataColumn\} usando el nombre de columna especificado y la tabla a la que pertenece.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | nombre del DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | la tabla a la que pertenece esta columna |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) usando el nombre de columna especificado y el tipo de datos.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | Una cadena que representa el nombre de la columna a crear. Si se establece en null o una cadena vacía (""), se especificará un nombre predeterminado al agregarla a la colección de columnas. |
| dataType | java.lang.Class | Un [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) compatible. |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Inicializa una nueva instancia de la clase [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) usando el nombre de columna especificado, el tipo de datos y la tabla de datos a la que pertenece.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | nombre del DataColumn |
| tipo | java.lang.Class | tipo de datos |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | la tabla a la que pertenece esta columna |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Obtiene un valor que indica si se permiten valores nulos en esta columna para las filas que pertenecen a la tabla.

**Returns:**
boolean - true si se permiten valores nulos; de lo contrario, false. El valor predeterminado es true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Obtiene un valor que indica si la columna incrementa automáticamente el valor de la columna para las nuevas filas añadidas a la tabla.

**Returns:**
boolean - true si el valor de la columna se incrementa automáticamente; de lo contrario, false. El valor predeterminado es false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Obtiene el valor inicial para una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true.

**Returns:**
long - El valor inicial para la característica [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean).
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Obtiene el incremento utilizado por una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true.

**Returns:**
long - El número por el cual el valor de la columna se incrementa automáticamente. El valor predeterminado es 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Obtiene el título de la columna.

**Returns:**
java.lang.String - La leyenda de la columna. Si no se establece, devuelve el valor de [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Obtiene el [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la columna.

**Returns:**
int - Uno de los valores de [MappingType](../../com.aspose.words.net.system.data/mappingtype/). El valor devuelto es una de las constantes de [MappingType](../../com.aspose.words.net.system.data/mappingtype/).
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Obtiene el nombre de la columna en la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
java.lang.String - El nombre de la columna.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Obtiene el tipo de datos almacenados en la columna.

**Returns:**
java.lang.Class - Un objeto java.lang.Class que representa el tipo de datos de la columna.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Obtiene el valor predeterminado para la columna al crear nuevas filas.

**Returns:**
java.lang.Object - Un valor apropiado para el [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) de la columna.
### getExpression() {#getExpression}
```
public String getExpression()
```


Obtiene la expresión utilizada para filtrar filas, calcular los valores en una columna o crear una columna agregada.

**Returns:**
java.lang.String - Una expresión para calcular el valor de una columna, o crear una columna agregada. El tipo de retorno de una expresión se determina por el [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) de la columna.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Obtiene la longitud máxima de una columna de texto.

**Returns:**
int - La longitud máxima de la columna en caracteres. Si la columna no tiene longitud máxima, el valor es -1 (predeterminado).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Obtiene el espacio de nombres del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Returns:**
java.lang.String - El espacio de nombres del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Obtiene la posición de la columna en la colección [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
int - La posición de la columna. Obtiene -1 si la columna no es miembro de una colección.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


Obtiene un prefijo XML que hace alias al espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - El prefijo XML para el espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/) namespace.
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Obtiene un valor que indica si la columna permite cambios tan pronto como se ha añadido una fila a la tabla.

**Returns:**
boolean - verdadero si la columna es de solo lectura; de lo contrario, falso. El valor predeterminado es falso.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtiene el [DataTable](../../com.aspose.words.net.system.data/datatable/) al que pertenece la columna.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Obtiene un valor que indica si los valores en cada fila de la columna deben ser únicos.

**Returns:**
boolean - verdadero si el valor debe ser único; de lo contrario, falso. El valor predeterminado es falso.
### isReadOnly() {#isReadOnly}
```
public boolean isReadOnly()
```




**Returns:**
boolean
### isUnique() {#isUnique}
```
public boolean isUnique()
```




**Returns:**
boolean
### setAllowDBNull(boolean value) {#setAllowDBNull-boolean}
```
public void setAllowDBNull(boolean value)
```


Establece un valor que indica si se permiten valores nulos en esta columna para las filas que pertenecen a la tabla.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | verdadero si se permiten valores nulos; de lo contrario, falso. El valor predeterminado es verdadero. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Establece un valor que indica si la columna incrementa automáticamente el valor de la columna para las nuevas filas añadidas a la tabla.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | verdadero si el valor de la columna se incrementa automáticamente; de lo contrario, falso. El valor predeterminado es falso. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Establece el valor inicial para una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | long | El valor inicial para la característica [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Establece el incremento utilizado por una columna que tiene su propiedad [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) establecida en true.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | long | El número por el cual el valor de la columna se incrementa automáticamente. El valor predeterminado es 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Establece el título de la columna.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El título de la columna. Si no se establece, devuelve el valor de [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String). |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Establece el [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la columna.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Uno de los valores de [MappingType](../../com.aspose.words.net.system.data/mappingtype/). El valor debe ser una de las constantes de [MappingType](../../com.aspose.words.net.system.data/mappingtype/). |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Establece el nombre de la columna en la [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre de la columna. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Establece el tipo de datos almacenados en la columna.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.Class | Un objeto java.lang.Class que representa el tipo de datos de la columna. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Establece el valor predeterminado para la columna al crear nuevas filas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.Object | Un valor apropiado para el [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Establece la longitud máxima de una columna de texto.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | La longitud máxima de la columna en caracteres. Si la columna no tiene longitud máxima, el valor es -1 (predeterminado). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Establece el espacio de nombres del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El espacio de nombres del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


Cambia el ordinal o la posición del [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) al ordinal o posición especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ordinal | int | El ordinal especificado. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


Establece un prefijo XML que actúa como alias del espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El prefijo XML para el espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Establece un valor que indica si la columna permite cambios tan pronto como se ha añadido una fila a la tabla.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | verdadero si la columna es de solo lectura; de lo contrario, falso. El valor predeterminado es falso. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Establece un valor que indica si los valores en cada fila de la columna deben ser únicos.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | verdadero si el valor debe ser único; de lo contrario, falso. El valor predeterminado es falso. |

### toString() {#toString}
```
public String toString()
```


Obtiene el [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) de la columna, si existe.

**Returns:**
java.lang.String - El valor de [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression), si la propiedad está establecida; de lo contrario, la propiedad [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
