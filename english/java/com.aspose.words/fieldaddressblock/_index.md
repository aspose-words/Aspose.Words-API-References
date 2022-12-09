---
title: FieldAddressBlock
second_title: Aspose.Words for Java API Reference
description: Implements the ADDRESSBLOCK field.
type: docs
weight: 154
url: /java/com.aspose.words/fieldaddressblock/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldAddressBlock extends Field
```

Implements the ADDRESSBLOCK field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

Represents an address block. An *address block* is a block of text specifying information appropriate for a postal mailing address, in the order required by the destination country.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getExcludedCountryOrRegionName()](#getExcludedCountryOrRegionName) | Gets the excluded country/region name. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldNames()](#getFieldNames) | Returns a collection of mail merge field names used by the field. |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getFormatAddressOnCountryOrRegion()](#getFormatAddressOnCountryOrRegion) | Gets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |
| [getIncludeCountryOrRegionName()](#getIncludeCountryOrRegionName) | Gets whether to include the name of the country/region. |
| [getLanguageId()](#getLanguageId) | Gets the language ID used to format the address. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getMergeFormat()](#getMergeFormat) |  |
| [getNameAndAddressFormat()](#getNameAndAddressFormat) | Gets the name and address format. |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [hashCode()](#hashCode) |  |
| [iFormattableMergeField_FetchDocument()](#iFormattableMergeField-FetchDocument) |  |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the field from the document. |
| [setExcludedCountryOrRegionName(String value)](#setExcludedCountryOrRegionName-java.lang.String) | Sets the excluded country/region name. |
| [setFormatAddressOnCountryOrRegion(boolean value)](#setFormatAddressOnCountryOrRegion-boolean) | Sets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |
| [setIncludeCountryOrRegionName(String value)](#setIncludeCountryOrRegionName-java.lang.String) | Sets whether to include the name of the country/region. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String) | Sets the language ID used to format the address. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setNameAndAddressFormat(String value)](#setNameAndAddressFormat-java.lang.String) | Sets the name and address format. |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [toString()](#toString) |  |
| [unlink()](#unlink) | Performs the field unlink. |
| [update()](#update) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Performs a field update. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend) - The node that represents the field end.
### getExcludedCountryOrRegionName() {#getExcludedCountryOrRegionName}
```
public String getExcludedCountryOrRegionName()
```


Gets the excluded country/region name.

**Returns:**
java.lang.String - The excluded country/region name.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ true  if child field codes should be included. |

**Returns:**
java.lang.String
### getFieldNames() {#getFieldNames}
```
public String[] getFieldNames()
```


Returns a collection of mail merge field names used by the field.

**Returns:**
java.lang.String[]
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat) - A [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.
### getFormatAddressOnCountryOrRegion() {#getFormatAddressOnCountryOrRegion}
```
public boolean getFormatAddressOnCountryOrRegion()
```


Gets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006).

**Returns:**
boolean - Whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006).
### getIncludeCountryOrRegionName() {#getIncludeCountryOrRegionName}
```
public String getIncludeCountryOrRegionName()
```


Gets whether to include the name of the country/region.

**Returns:**
java.lang.String - Whether to include the name of the country/region.
### getLanguageId() {#getLanguageId}
```
public String getLanguageId()
```


Gets the language ID used to format the address.

**Returns:**
java.lang.String - The language ID used to format the address.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### getMergeFormat() {#getMergeFormat}
```
public String getMergeFormat()
```




**Returns:**
java.lang.String
### getNameAndAddressFormat() {#getNameAndAddressFormat}
```
public String getNameAndAddressFormat()
```


Gets the name and address format.

**Returns:**
java.lang.String - The name and address format.
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### iFormattableMergeField_FetchDocument() {#iFormattableMergeField-FetchDocument}
```
public Document iFormattableMergeField_FetchDocument()
```




**Returns:**
[Document](../../com.aspose.words/document)
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove() {#remove}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns  null .

**Returns:**
[Node](../../com.aspose.words/node)
### setExcludedCountryOrRegionName(String value) {#setExcludedCountryOrRegionName-java.lang.String}
```
public void setExcludedCountryOrRegionName(String value)
```


Sets the excluded country/region name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The excluded country/region name. |

### setFormatAddressOnCountryOrRegion(boolean value) {#setFormatAddressOnCountryOrRegion-boolean}
```
public void setFormatAddressOnCountryOrRegion(boolean value)
```


Sets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |

### setIncludeCountryOrRegionName(String value) {#setIncludeCountryOrRegionName-java.lang.String}
```
public void setIncludeCountryOrRegionName(String value)
```


Sets whether to include the name of the country/region.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Whether to include the name of the country/region. |

### setLanguageId(String value) {#setLanguageId-java.lang.String}
```
public void setLanguageId(String value)
```


Sets the language ID used to format the address.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The language ID used to format the address. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setNameAndAddressFormat(String value) {#setNameAndAddressFormat-java.lang.String}
```
public void setNameAndAddressFormat(String value)
```


Sets the name and address format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name and address format. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### unlink() {#unlink}
```
public boolean unlink()
```


Performs the field unlink.

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean - \{ true  if the field has been unlinked, otherwise  false .
### update() {#update}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

