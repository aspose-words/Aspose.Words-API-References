---
title: TxtSaveOptionsBase
second_title: Aspose.Words for Java API Reference
description: The base class for specifying additional options when saving a document into a text based formats.
type: docs
weight: 586
url: /java/com.aspose.words/txtsaveoptionsbase/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public abstract class TxtSaveOptionsBase extends SaveOptions
```

The base class for specifying additional options when saving a document into a text based formats.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [TxtSaveOptionsBase()](#TxtSaveOptionsBase--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getEncoding()](#getEncoding--) |  |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [getParagraphBreak()](#getParagraphBreak--) | Specifies the string to use as a paragraph break when exporting in text formats. |
| [setParagraphBreak(String value)](#setParagraphBreak-java.lang.String-) | Specifies the string to use as a paragraph break when exporting in text formats. |
| [getForcePageBreaks()](#getForcePageBreaks--) | Allows to specify whether the page breaks should be preserved during export. |
| [setForcePageBreaks(boolean value)](#setForcePageBreaks-boolean-) | Allows to specify whether the page breaks should be preserved during export. |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode--) | Specifies the way headers and footers are exported to the text formats. |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int-) | Specifies the way headers and footers are exported to the text formats. |
### TxtSaveOptionsBase() {#TxtSaveOptionsBase--}
```
public TxtSaveOptionsBase()
```


### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### getParagraphBreak() {#getParagraphBreak--}
```
public String getParagraphBreak()
```


Specifies the string to use as a paragraph break when exporting in text formats.

The default value is [ControlChar.CR\_LF](../../com.aspose.words/controlchar\#CR-LF).

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setParagraphBreak(String value) {#setParagraphBreak-java.lang.String-}
```
public void setParagraphBreak(String value)
```


Specifies the string to use as a paragraph break when exporting in text formats.

The default value is [ControlChar.CR\_LF](../../com.aspose.words/controlchar\#CR-LF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getForcePageBreaks() {#getForcePageBreaks--}
```
public boolean getForcePageBreaks()
```


Allows to specify whether the page breaks should be preserved during export.

The default value is **false**.

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

**Returns:**
boolean - The corresponding  boolean  value.
### setForcePageBreaks(boolean value) {#setForcePageBreaks-boolean-}
```
public void setForcePageBreaks(boolean value)
```


Allows to specify whether the page breaks should be preserved during export.

The default value is **false**.

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportHeadersFootersMode() {#getExportHeadersFootersMode--}
```
public int getExportHeadersFootersMode()
```


Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY\_ONLY](../../com.aspose.words/txtexportheadersfootersmode\#PRIMARY-ONLY).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TxtExportHeadersFootersMode](../../com.aspose.words/txtexportheadersfootersmode) constants.
### setExportHeadersFootersMode(int value) {#setExportHeadersFootersMode-int-}
```
public void setExportHeadersFootersMode(int value)
```


Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY\_ONLY](../../com.aspose.words/txtexportheadersfootersmode\#PRIMARY-ONLY).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TxtExportHeadersFootersMode](../../com.aspose.words/txtexportheadersfootersmode) constants. |

