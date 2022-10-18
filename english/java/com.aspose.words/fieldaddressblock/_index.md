---
title: FieldAddressBlock
second_title: Aspose.Words for Java API Reference
description: Implements the ADDRESSBLOCK field.
type: docs
weight: 153
url: /java/com.aspose.words/fieldaddressblock/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldAddressBlock extends Field
```

Implements the ADDRESSBLOCK field.

To learn more, visit the **Working with Fields** documentation article.

Represents an address block. An *address block* is a block of text specifying information appropriate for a postal mailing address, in the order required by the destination country.
## Methods

| Method | Description |
| --- | --- |
| [getFormatAddressOnCountryOrRegion()](#getFormatAddressOnCountryOrRegion--) | Gets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |
| [setFormatAddressOnCountryOrRegion(boolean value)](#setFormatAddressOnCountryOrRegion-boolean-) | Sets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |
| [getIncludeCountryOrRegionName()](#getIncludeCountryOrRegionName--) | Gets whether to include the name of the country/region. |
| [setIncludeCountryOrRegionName(String value)](#setIncludeCountryOrRegionName-java.lang.String-) | Sets whether to include the name of the country/region. |
| [getExcludedCountryOrRegionName()](#getExcludedCountryOrRegionName--) | Gets the excluded country/region name. |
| [setExcludedCountryOrRegionName(String value)](#setExcludedCountryOrRegionName-java.lang.String-) | Sets the excluded country/region name. |
| [getNameAndAddressFormat()](#getNameAndAddressFormat--) | Gets the name and address format. |
| [setNameAndAddressFormat(String value)](#setNameAndAddressFormat-java.lang.String-) | Sets the name and address format. |
| [getLanguageId()](#getLanguageId--) | Gets the language ID used to format the address. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String-) | Sets the language ID used to format the address. |
| [getFieldNames()](#getFieldNames--) | Returns a collection of mail merge field names used by the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [iFormattableMergeField_FetchDocument()](#iFormattableMergeField-FetchDocument--) |  |
| [getMergeFormat()](#getMergeFormat--) |  |
### getFormatAddressOnCountryOrRegion() {#getFormatAddressOnCountryOrRegion--}
```
public boolean getFormatAddressOnCountryOrRegion()
```


Gets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006).

**Returns:**
boolean - Whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006).
### setFormatAddressOnCountryOrRegion(boolean value) {#setFormatAddressOnCountryOrRegion-boolean-}
```
public void setFormatAddressOnCountryOrRegion(boolean value)
```


Sets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |

### getIncludeCountryOrRegionName() {#getIncludeCountryOrRegionName--}
```
public String getIncludeCountryOrRegionName()
```


Gets whether to include the name of the country/region.

**Returns:**
java.lang.String - Whether to include the name of the country/region.
### setIncludeCountryOrRegionName(String value) {#setIncludeCountryOrRegionName-java.lang.String-}
```
public void setIncludeCountryOrRegionName(String value)
```


Sets whether to include the name of the country/region.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Whether to include the name of the country/region. |

### getExcludedCountryOrRegionName() {#getExcludedCountryOrRegionName--}
```
public String getExcludedCountryOrRegionName()
```


Gets the excluded country/region name.

**Returns:**
java.lang.String - The excluded country/region name.
### setExcludedCountryOrRegionName(String value) {#setExcludedCountryOrRegionName-java.lang.String-}
```
public void setExcludedCountryOrRegionName(String value)
```


Sets the excluded country/region name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The excluded country/region name. |

### getNameAndAddressFormat() {#getNameAndAddressFormat--}
```
public String getNameAndAddressFormat()
```


Gets the name and address format.

**Returns:**
java.lang.String - The name and address format.
### setNameAndAddressFormat(String value) {#setNameAndAddressFormat-java.lang.String-}
```
public void setNameAndAddressFormat(String value)
```


Sets the name and address format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name and address format. |

### getLanguageId() {#getLanguageId--}
```
public String getLanguageId()
```


Gets the language ID used to format the address.

**Returns:**
java.lang.String - The language ID used to format the address.
### setLanguageId(String value) {#setLanguageId-java.lang.String-}
```
public void setLanguageId(String value)
```


Sets the language ID used to format the address.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The language ID used to format the address. |

### getFieldNames() {#getFieldNames--}
```
public String[] getFieldNames()
```


Returns a collection of mail merge field names used by the field.

**Returns:**
java.lang.String[]
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
### iFormattableMergeField_FetchDocument() {#iFormattableMergeField-FetchDocument--}
```
public Document iFormattableMergeField_FetchDocument()
```




**Returns:**
[Document](../../com.aspose.words/document)
### getMergeFormat() {#getMergeFormat--}
```
public String getMergeFormat()
```




**Returns:**
java.lang.String
