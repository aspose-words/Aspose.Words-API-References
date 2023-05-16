---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
second_title: Aspose.Words for Java
description: Represents options for parsing JSON data in Java.
type: docs
weight: 365
url: /java/com.aspose.words/jsondataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataLoadOptions
```

Represents options for parsing JSON data.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.

 **Remarks:** 

An instance of this class can be passed into constructors of [JsonDataSource](../../com.aspose.words/jsondatasource/).


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [JsonDataLoadOptions()](#JsonDataLoadOptions) | Initializes a new instance of this class with default options. |
## Methods

| Method | Description |
| --- | --- |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject) | Gets a flag indicating whether a generated data source will always contain an object for a JSON root element. |
| [getExactDateTimeParseFormats()](#getExactDateTimeParseFormats) | Gets exact formats for parsing JSON date-time values while loading JSON. |
| [getSimpleValueParseMode()](#getSimpleValueParseMode) | Gets a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean) | Sets a flag indicating whether a generated data source will always contain an object for a JSON root element. |
| [setExactDateTimeParseFormats(Iterable value)](#setExactDateTimeParseFormats-java.lang.Iterable) | Sets exact formats for parsing JSON date-time values while loading JSON. |
| [setSimpleValueParseMode(int value)](#setSimpleValueParseMode-int) | Sets a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. |
### JsonDataLoadOptions() {#JsonDataLoadOptions}
```
public JsonDataLoadOptions()
```


Initializes a new instance of this class with default options.

### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject}
```
public boolean getAlwaysGenerateRootObject()
```


Gets a flag indicating whether a generated data source will always contain an object for a JSON root element. If a JSON root element contains a single complex property, such an object is not created by default.

 **Remarks:** 

The default value is  false .

**Returns:**
boolean - A flag indicating whether a generated data source will always contain an object for a JSON root element.
### getExactDateTimeParseFormats() {#getExactDateTimeParseFormats}
```
public Iterable getExactDateTimeParseFormats()
```


Gets exact formats for parsing JSON date-time values while loading JSON. The default is  null .

 **Remarks:** 

Strings encoded using Microsoft® JSON date-time format (for example, "/Date(1224043200000)/") are always recognized as date-time values regardless of a value of this property. The property defines additional formats to be used while parsing date-time values from strings in the following way:

 *  When [getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions/\#getExactDateTimeParseFormats) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions/\#setExactDateTimeParseFormats-java.lang.Iterable) is  null , the ISO-8601 format and all date-time formats supported for the current, English USA, and English New Zealand cultures are used additionally in the mentioned order.
 *  When [getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions/\#getExactDateTimeParseFormats) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions/\#setExactDateTimeParseFormats-java.lang.Iterable) contains strings, they are used as additional date-time formats utilizing the current culture.
 *  When [getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions/\#getExactDateTimeParseFormats) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions/\#setExactDateTimeParseFormats-java.lang.Iterable) is empty, no additional date-time formats are used.

**Returns:**
java.lang.Iterable - Exact formats for parsing JSON date-time values while loading JSON.
### getSimpleValueParseMode() {#getSimpleValueParseMode}
```
public int getSimpleValueParseMode()
```


Gets a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. Such a mode does not affect parsing of date-time values. The default is [JsonSimpleValueParseMode.LOOSE](../../com.aspose.words/jsonsimplevalueparsemode/\#LOOSE).

**Returns:**
int - A mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. The returned value is one of [JsonSimpleValueParseMode](../../com.aspose.words/jsonsimplevalueparsemode/) constants.
### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean}
```
public void setAlwaysGenerateRootObject(boolean value)
```


Sets a flag indicating whether a generated data source will always contain an object for a JSON root element. If a JSON root element contains a single complex property, such an object is not created by default.

 **Remarks:** 

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether a generated data source will always contain an object for a JSON root element. |

### setExactDateTimeParseFormats(Iterable value) {#setExactDateTimeParseFormats-java.lang.Iterable}
```
public void setExactDateTimeParseFormats(Iterable value)
```


Sets exact formats for parsing JSON date-time values while loading JSON. The default is  null .

 **Remarks:** 

Strings encoded using Microsoft® JSON date-time format (for example, "/Date(1224043200000)/") are always recognized as date-time values regardless of a value of this property. The property defines additional formats to be used while parsing date-time values from strings in the following way:

 *  When [getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions/\#getExactDateTimeParseFormats) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions/\#setExactDateTimeParseFormats-java.lang.Iterable) is  null , the ISO-8601 format and all date-time formats supported for the current, English USA, and English New Zealand cultures are used additionally in the mentioned order.
 *  When [getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions/\#getExactDateTimeParseFormats) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions/\#setExactDateTimeParseFormats-java.lang.Iterable) contains strings, they are used as additional date-time formats utilizing the current culture.
 *  When [getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions/\#getExactDateTimeParseFormats) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions/\#setExactDateTimeParseFormats-java.lang.Iterable) is empty, no additional date-time formats are used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Iterable | Exact formats for parsing JSON date-time values while loading JSON. |

### setSimpleValueParseMode(int value) {#setSimpleValueParseMode-int}
```
public void setSimpleValueParseMode(int value)
```


Sets a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. Such a mode does not affect parsing of date-time values. The default is [JsonSimpleValueParseMode.LOOSE](../../com.aspose.words/jsonsimplevalueparsemode/\#LOOSE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. The value must be one of [JsonSimpleValueParseMode](../../com.aspose.words/jsonsimplevalueparsemode/) constants. |

