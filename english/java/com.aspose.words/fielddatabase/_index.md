---
title: FieldDatabase
second_title: Aspose.Words for Java API Reference
description: Implements the DATABASE field.
type: docs
weight: 174
url: /java/com.aspose.words/fielddatabase/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldDatabase extends Field
```

Implements the DATABASE field.

To learn more, visit the **Working with Fields** documentation article.

Inserts the results of a database query into a WordprocessingML table.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getConnection()](#getConnection--) | Gets a connection to the data. |
| [getDisplayResult()](#getDisplayResult--) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd--) | Gets the node that represents the field end. |
| [getFieldCode()](#getFieldCode--) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFileName()](#getFileName--) | Gets the complete path and file name of the database |
| [getFirstRecord()](#getFirstRecord--) | Gets the integral record number of the first data record to insert. |
| [getFormat()](#getFormat--) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getFormatAttributes()](#getFormatAttributes--) | Gets which attributes of the format are to be applied to the table. |
| [getInsertHeadings()](#getInsertHeadings--) | Gets whether to insert the field names from the database as column headings in the resulting table. |
| [getInsertOnceOnMailMerge()](#getInsertOnceOnMailMerge--) | Gets whether to insert data at the beginning of a merge. |
| [getLastRecord()](#getLastRecord--) | Gets the integral record number of the last data record to insert. |
| [getLocaleId()](#getLocaleId--) | Gets the LCID of the field. |
| [getQuery()](#getQuery--) | Gets a set of SQL instructions that query the database. |
| [getResult()](#getResult--) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator--) | Gets the node that represents the field separator. |
| [getStart()](#getStart--) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getTableFormat()](#getTableFormat--) | Gets the format that is to be applied to the result of the database query. |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [hashCode()](#hashCode--) |  |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked--) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Removes the field from the document. |
| [setConnection(String value)](#setConnection-java.lang.String-) | Sets a connection to the data. |
| [setFileName(String value)](#setFileName-java.lang.String-) | Sets the complete path and file name of the database |
| [setFirstRecord(String value)](#setFirstRecord-java.lang.String-) | Sets the integral record number of the first data record to insert. |
| [setFormatAttributes(String value)](#setFormatAttributes-java.lang.String-) | Sets which attributes of the format are to be applied to the table. |
| [setInsertHeadings(boolean value)](#setInsertHeadings-boolean-) | Sets whether to insert the field names from the database as column headings in the resulting table. |
| [setInsertOnceOnMailMerge(boolean value)](#setInsertOnceOnMailMerge-boolean-) | Sets whether to insert data at the beginning of a merge. |
| [setLastRecord(String value)](#setLastRecord-java.lang.String-) | Sets the integral record number of the last data record to insert. |
| [setLocaleId(int value)](#setLocaleId-int-) | Sets the LCID of the field. |
| [setQuery(String value)](#setQuery-java.lang.String-) | Sets a set of SQL instructions that query the database. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets text that is between the field separator and field end. |
| [setTableFormat(String value)](#setTableFormat-java.lang.String-) | Sets the format that is to be applied to the result of the database query. |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | Performs the field unlink. |
| [update()](#update--) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | Performs a field update. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getConnection() {#getConnection--}
```
public String getConnection()
```


Gets a connection to the data.

**Returns:**
java.lang.String - A connection to the data.
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend) - The node that represents the field end.
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ True  if child field codes should be included. |

**Returns:**
java.lang.String
### getFileName() {#getFileName--}
```
public String getFileName()
```


Gets the complete path and file name of the database

**Returns:**
java.lang.String - The complete path and file name of the database
### getFirstRecord() {#getFirstRecord--}
```
public String getFirstRecord()
```


Gets the integral record number of the first data record to insert.

**Returns:**
java.lang.String - The integral record number of the first data record to insert.
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat) - A [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.
### getFormatAttributes() {#getFormatAttributes--}
```
public String getFormatAttributes()
```


Gets which attributes of the format are to be applied to the table.

**Returns:**
java.lang.String - Which attributes of the format are to be applied to the table.
### getInsertHeadings() {#getInsertHeadings--}
```
public boolean getInsertHeadings()
```


Gets whether to insert the field names from the database as column headings in the resulting table.

**Returns:**
boolean - Whether to insert the field names from the database as column headings in the resulting table.
### getInsertOnceOnMailMerge() {#getInsertOnceOnMailMerge--}
```
public boolean getInsertOnceOnMailMerge()
```


Gets whether to insert data at the beginning of a merge.

**Returns:**
boolean - Whether to insert data at the beginning of a merge.
### getLastRecord() {#getLastRecord--}
```
public String getLastRecord()
```


Gets the integral record number of the last data record to insert.

**Returns:**
java.lang.String - The integral record number of the last data record to insert.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getQuery() {#getQuery--}
```
public String getQuery()
```


Gets a set of SQL instructions that query the database.

**Returns:**
java.lang.String - A set of SQL instructions that query the database.
### getResult() {#getResult--}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be null.

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getTableFormat() {#getTableFormat--}
```
public String getTableFormat()
```


Gets the format that is to be applied to the result of the database query.

**Returns:**
java.lang.String - The format that is to be applied to the result of the database query.
### getType() {#getType--}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.

**Returns:**
[Node](../../com.aspose.words/node)
### setConnection(String value) {#setConnection-java.lang.String-}
```
public void setConnection(String value)
```


Sets a connection to the data.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A connection to the data. |

### setFileName(String value) {#setFileName-java.lang.String-}
```
public void setFileName(String value)
```


Sets the complete path and file name of the database

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The complete path and file name of the database |

### setFirstRecord(String value) {#setFirstRecord-java.lang.String-}
```
public void setFirstRecord(String value)
```


Sets the integral record number of the first data record to insert.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The integral record number of the first data record to insert. |

### setFormatAttributes(String value) {#setFormatAttributes-java.lang.String-}
```
public void setFormatAttributes(String value)
```


Sets which attributes of the format are to be applied to the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Which attributes of the format are to be applied to the table. |

### setInsertHeadings(boolean value) {#setInsertHeadings-boolean-}
```
public void setInsertHeadings(boolean value)
```


Sets whether to insert the field names from the database as column headings in the resulting table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to insert the field names from the database as column headings in the resulting table. |

### setInsertOnceOnMailMerge(boolean value) {#setInsertOnceOnMailMerge-boolean-}
```
public void setInsertOnceOnMailMerge(boolean value)
```


Sets whether to insert data at the beginning of a merge.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to insert data at the beginning of a merge. |

### setLastRecord(String value) {#setLastRecord-java.lang.String-}
```
public void setLastRecord(String value)
```


Sets the integral record number of the last data record to insert.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The integral record number of the last data record to insert. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setQuery(String value) {#setQuery-java.lang.String-}
```
public void setQuery(String value)
```


Sets a set of SQL instructions that query the database.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A set of SQL instructions that query the database. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setTableFormat(String value) {#setTableFormat-java.lang.String-}
```
public void setTableFormat(String value)
```


Sets the format that is to be applied to the result of the database query.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The format that is to be applied to the result of the database query. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### unlink() {#unlink--}
```
public boolean unlink()
```


Performs the field unlink.

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean - \{ True  if the field has been unlinked, otherwise  false .
### update() {#update--}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

