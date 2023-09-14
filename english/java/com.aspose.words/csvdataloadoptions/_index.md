---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
second_title: Aspose.Words for Java
description: Represents options for parsing CSV data in Java.
type: docs
weight: 112
url: /java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Represents options for parsing CSV data.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.

 **Remarks:** 

An instance of this class can be passed into constructors of [CsvDataSource](../../com.aspose.words/csvdatasource/).


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Initializes a new instance of this class with default options. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Initializes a new instance of this class with specifying whether CSV data contains column names at the first line. |
## Methods

| Method | Description |
| --- | --- |
| [getCommentChar()](#getCommentChar) | Gets the character that is used to comment lines of CSV data. |
| [getDelimiter()](#getDelimiter) | Gets the character to be used as a column delimiter. |
| [getQuoteChar()](#getQuoteChar) | Gets the character that is used to quote field values. |
| [hasHeaders()](#hasHeaders) | Gets a value indicating whether the first record of CSV data contains column names. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | Sets a value indicating whether the first record of CSV data contains column names. |
| [setCommentChar(char value)](#setCommentChar-char) | Sets the character that is used to comment lines of CSV data. |
| [setDelimiter(char value)](#setDelimiter-char) | Sets the character to be used as a column delimiter. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Sets the character that is used to quote field values. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Initializes a new instance of this class with default options.

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


Initializes a new instance of this class with specifying whether CSV data contains column names at the first line.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


Gets the character that is used to comment lines of CSV data.

 **Remarks:** 

The default value is '\#' (number sign).

**Returns:**
char - The character that is used to comment lines of CSV data.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Gets the character to be used as a column delimiter.

 **Remarks:** 

The default value is ',' (comma).

**Returns:**
char - The character to be used as a column delimiter.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Gets the character that is used to quote field values.

 **Remarks:** 

The default value is '"' (quotation mark).

Double the character to place it into quoted text.

**Returns:**
char - The character that is used to quote field values.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


Gets a value indicating whether the first record of CSV data contains column names.

 **Remarks:** 

The default value is  false .

**Returns:**
boolean - A value indicating whether the first record of CSV data contains column names.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


Sets a value indicating whether the first record of CSV data contains column names.

 **Remarks:** 

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the first record of CSV data contains column names. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


Sets the character that is used to comment lines of CSV data.

 **Remarks:** 

The default value is '\#' (number sign).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | char | The character that is used to comment lines of CSV data. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Sets the character to be used as a column delimiter.

 **Remarks:** 

The default value is ',' (comma).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | char | The character to be used as a column delimiter. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Sets the character that is used to quote field values.

 **Remarks:** 

The default value is '"' (quotation mark).

Double the character to place it into quoted text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | char | The character that is used to quote field values. |

