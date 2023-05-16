---
title: DataColumn
linktitle: DataColumn
second_title: Aspose.Words for Java
description: Represents the schema of a column in a DataTable in Java.
type: docs
weight: 14
url: /java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Represents the schema of a column in a [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Constructors

| Constructor | Description |
| --- | --- |
| [DataColumn()](#DataColumn) | Initializes a new instance of a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class as type string. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Inititalizes a new instance of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class, as type string, using the specified column name. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Initializes a new instance of the @\{link DataColumn\} class using the specified column name and table it belongs to. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Inititalizes a new instance of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class using the specified column name and data type. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Initializes a new instance of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class using the specified column name, data type and data table it belongs to. |
## Methods

| Method | Description |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Gets a value that indicates whether null values are allowed in this column for rows that belong to the table. |
| [getAutoIncrement()](#getAutoIncrement) | Gets a value that indicates whether the column automatically increments the value of the column for new rows added to the table. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Gets the starting value for a column that has its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Gets the increment used by a column with its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true. |
| [getCaption()](#getCaption) | Gets the caption for the column. |
| [getColumnMapping()](#getColumnMapping) | Gets the [MappingType](../../com.aspose.words.net.system.data/mappingtype/) of the column. |
| [getColumnName()](#getColumnName) | Gets the name of the column in the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getDataType()](#getDataType) | Gets the type of data stored in the column. |
| [getDefaultValue()](#getDefaultValue) | Gets the default value for the column when you are creating new rows. |
| [getExpression()](#getExpression) | Gets the expression used to filter rows, calculate the values in a column, or create an aggregate column. |
| [getMaxLength()](#getMaxLength) | Gets the maximum length of a text column. |
| [getNamespace()](#getNamespace) | Gets the namespace of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [getOrdinal()](#getOrdinal) | Gets the position of the column in the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) collection. |
| [getPrefix()](#getPrefix) | Gets an XML prefix that aliases the namespace of the [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getReadOnly()](#getReadOnly) | Gets a value that indicates whether the column allows for changes as soon as a row has been added to the table. |
| [getTable()](#getTable) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the column belongs to. |
| [getUnique()](#getUnique) | Gets a value that indicates whether the values in each row of the column must be unique. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Sets a value that indicates whether null values are allowed in this column for rows that belong to the table. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Sets a value that indicates whether the column automatically increments the value of the column for new rows added to the table. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Sets the starting value for a column that has its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Sets the increment used by a column with its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true. |
| [setCaption(String value)](#setCaption-java.lang.String) | Sets the caption for the column. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Sets the [MappingType](../../com.aspose.words.net.system.data/mappingtype/) of the column. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Sets the name of the column in the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Sets the type of data stored in the column. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Sets the default value for the column when you are creating new rows. |
| [setMaxLength(int value)](#setMaxLength-int) | Sets the maximum length of a text column. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Sets the namespace of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [setOrdinal(int ordinal)](#setOrdinal-int) | Changes the ordinal or position of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) to the specified ordinal or position. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | Sets an XML prefix that aliases the namespace of the [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Sets a value that indicates whether the column allows for changes as soon as a row has been added to the table. |
| [setUnique(boolean value)](#setUnique-boolean) | Sets a value that indicates whether the values in each row of the column must be unique. |
| [toString()](#toString) | Gets the [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) of the column, if one exists. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Initializes a new instance of a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class as type string.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Inititalizes a new instance of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class, as type string, using the specified column name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | A string that represents the name of the column to be created. If set to null or an empty string (""), a default name will be specified when added to the columns collection. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Initializes a new instance of the @\{link DataColumn\} class using the specified column name and table it belongs to.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | name of the DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | the table this column belongs to |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Inititalizes a new instance of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class using the specified column name and data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | A string that represents the name of the column to be created. If set to null or an empty string (""), a default name will be specified when added to the columns collection. |
| dataType | java.lang.Class | A supported [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Initializes a new instance of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) class using the specified column name, data type and data table it belongs to.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | name of the DataColumn |
| type | java.lang.Class | data type |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | the table this column belongs to |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Gets a value that indicates whether null values are allowed in this column for rows that belong to the table.

**Returns:**
boolean - true if null values values are allowed; otherwise, false. The default is true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Gets a value that indicates whether the column automatically increments the value of the column for new rows added to the table.

**Returns:**
boolean - true if the value of the column increments automatically; otherwise, false. The default is false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Gets the starting value for a column that has its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true.

**Returns:**
long - The starting value for the [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) feature.
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Gets the increment used by a column with its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true.

**Returns:**
long - The number by which the value of the column is automatically incremented. The default is 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Gets the caption for the column.

**Returns:**
java.lang.String - The caption of the column. If not set, returns the [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) value.
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Gets the [MappingType](../../com.aspose.words.net.system.data/mappingtype/) of the column.

**Returns:**
int - One of the [MappingType](../../com.aspose.words.net.system.data/mappingtype/) values. The returned value is one of [MappingType](../../com.aspose.words.net.system.data/mappingtype/) constants.
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Gets the name of the column in the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
java.lang.String - The name of the column.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Gets the type of data stored in the column.

**Returns:**
java.lang.Class - A java.lang.Class object that represents the column data type.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Gets the default value for the column when you are creating new rows.

**Returns:**
java.lang.Object - A value appropriate to the column's [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class).
### getExpression() {#getExpression}
```
public String getExpression()
```


Gets the expression used to filter rows, calculate the values in a column, or create an aggregate column.

**Returns:**
java.lang.String - An expression to calculate the value of a column, or create an aggregate column. The return type of an expression is determined by the [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) of the column.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Gets the maximum length of a text column.

**Returns:**
int - The maximum length of the column in characters. If the column has no maximum length, the value is -1 (default).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Gets the namespace of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Returns:**
java.lang.String - The namespace of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Gets the position of the column in the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) collection.

**Returns:**
int - The position of the column. Gets -1 if the column is not a member of a collection.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


Gets an XML prefix that aliases the namespace of the [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - The XML prefix for the [DataTable](../../com.aspose.words.net.system.data/datatable/) namespace.
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Gets a value that indicates whether the column allows for changes as soon as a row has been added to the table.

**Returns:**
boolean - true if the column is read only; otherwise, false. The default is false.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the column belongs to.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Gets a value that indicates whether the values in each row of the column must be unique.

**Returns:**
boolean - true if the value must be unique; otherwise, false. The default is false.
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


Sets a value that indicates whether null values are allowed in this column for rows that belong to the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | true if null values values are allowed; otherwise, false. The default is true. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Sets a value that indicates whether the column automatically increments the value of the column for new rows added to the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | true if the value of the column increments automatically; otherwise, false. The default is false. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Sets the starting value for a column that has its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | long | The starting value for the [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) feature. |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Sets the increment used by a column with its [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) property set to true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | long | The number by which the value of the column is automatically incremented. The default is 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Sets the caption for the column.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The caption of the column. If not set, returns the [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) value. |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Sets the [MappingType](../../com.aspose.words.net.system.data/mappingtype/) of the column.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | One of the [MappingType](../../com.aspose.words.net.system.data/mappingtype/) values. The value must be one of [MappingType](../../com.aspose.words.net.system.data/mappingtype/) constants. |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Sets the name of the column in the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the column. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Sets the type of data stored in the column.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Class | A java.lang.Class object that represents the column data type. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Sets the default value for the column when you are creating new rows.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | A value appropriate to the column's [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Sets the maximum length of a text column.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The maximum length of the column in characters. If the column has no maximum length, the value is -1 (default). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Sets the namespace of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The namespace of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


Changes the ordinal or position of the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) to the specified ordinal or position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ordinal | int | The specified ordinal. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


Sets an XML prefix that aliases the namespace of the [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The XML prefix for the [DataTable](../../com.aspose.words.net.system.data/datatable/) namespace. |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Sets a value that indicates whether the column allows for changes as soon as a row has been added to the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | true if the column is read only; otherwise, false. The default is false. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Sets a value that indicates whether the values in each row of the column must be unique.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | true if the value must be unique; otherwise, false. The default is false. |

### toString() {#toString}
```
public String toString()
```


Gets the [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) of the column, if one exists.

**Returns:**
java.lang.String - The [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) value, if the property is set; otherwise, the [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) property.
