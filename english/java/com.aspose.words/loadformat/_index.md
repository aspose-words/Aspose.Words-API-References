---
title: LoadFormat
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 377
url: /java/com.aspose.words/loadformat/
---

**Inheritance:**
java.lang.Object
```
public class LoadFormat
```

A utility class providing constants. Indicates the format of the document that is to be loaded.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Instructs Aspose.Words to recognize the format automatically. |
| [DOC](#DOC) | Microsoft Word 95 or Word 97 - 2003 Document. |
| [DOT](#DOT) | Microsoft Word 95 or Word 97 - 2003 Template. |
| [DOC_PRE_WORD_60](#DOC-PRE-WORD-60) | The document is in pre-Word 95 format. |
| [DOCX](#DOCX) | Office Open XML WordprocessingML Document (macro-free). |
| [DOCM](#DOCM) | Office Open XML WordprocessingML Macro-Enabled Document. |
| [DOTX](#DOTX) | Office Open XML WordprocessingML Template (macro-free). |
| [DOTM](#DOTM) | Office Open XML WordprocessingML Macro-Enabled Template. |
| [FLAT_OPC](#FLAT-OPC) | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_MACRO_ENABLED](#FLAT-OPC-MACRO-ENABLED) | Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE](#FLAT-OPC-TEMPLATE) | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| [FLAT_OPC_TEMPLATE_MACRO_ENABLED](#FLAT-OPC-TEMPLATE-MACRO-ENABLED) | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| [RTF](#RTF) | RTF format. |
| [WORD_ML](#WORD-ML) | Microsoft Word 2003 WordprocessingML format. |
| [HTML](#HTML) | HTML format. |
| [MHTML](#MHTML) | MHTML (Web archive) format. |
| [MOBI](#MOBI) | MOBI format. |
| [CHM](#CHM) | CHM (Compiled HTML Help) format. |
| [AZW_3](#AZW-3) | AZW3 format. |
| [EPUB](#EPUB) | EPUB format. |
| [ODT](#ODT) | ODF Text Document. |
| [OTT](#OTT) | ODF Text Document Template. |
| [TEXT](#TEXT) | Plain Text. |
| [MARKDOWN](#MARKDOWN) | Markdown text document. |
| [PDF](#PDF) | Pdf document. |
| [XML](#XML) | XML document. |
| [UNKNOWN](#UNKNOWN) | Unrecognized format, cannot be loaded by Aspose.Words. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int loadFormat)](#getName-int-) |  |
| [toString(int loadFormat)](#toString-int-) |  |
| [fromName(String loadFormatName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Instructs Aspose.Words to recognize the format automatically.

### DOC {#DOC}
```
public static int DOC
```


Microsoft Word 95 or Word 97 - 2003 Document.

### DOT {#DOT}
```
public static int DOT
```


Microsoft Word 95 or Word 97 - 2003 Template.

### DOC_PRE_WORD_60 {#DOC-PRE-WORD-60}
```
public static int DOC_PRE_WORD_60
```


The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents.

### DOCX {#DOCX}
```
public static int DOCX
```


Office Open XML WordprocessingML Document (macro-free).

### DOCM {#DOCM}
```
public static int DOCM
```


Office Open XML WordprocessingML Macro-Enabled Document.

### DOTX {#DOTX}
```
public static int DOTX
```


Office Open XML WordprocessingML Template (macro-free).

### DOTM {#DOTM}
```
public static int DOTM
```


Office Open XML WordprocessingML Macro-Enabled Template.

### FLAT_OPC {#FLAT-OPC}
```
public static int FLAT_OPC
```


Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_MACRO_ENABLED {#FLAT-OPC-MACRO-ENABLED}
```
public static int FLAT_OPC_MACRO_ENABLED
```


Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_TEMPLATE {#FLAT-OPC-TEMPLATE}
```
public static int FLAT_OPC_TEMPLATE
```


Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package.

### FLAT_OPC_TEMPLATE_MACRO_ENABLED {#FLAT-OPC-TEMPLATE-MACRO-ENABLED}
```
public static int FLAT_OPC_TEMPLATE_MACRO_ENABLED
```


Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package.

### RTF {#RTF}
```
public static int RTF
```


RTF format.

### WORD_ML {#WORD-ML}
```
public static int WORD_ML
```


Microsoft Word 2003 WordprocessingML format.

### HTML {#HTML}
```
public static int HTML
```


HTML format.

### MHTML {#MHTML}
```
public static int MHTML
```


MHTML (Web archive) format.

### MOBI {#MOBI}
```
public static int MOBI
```


MOBI format. Used by MobiPocket reader and Amazon Kindle readers.

### CHM {#CHM}
```
public static int CHM
```


CHM (Compiled HTML Help) format.

### AZW_3 {#AZW-3}
```
public static int AZW_3
```


AZW3 format. Used by Amazon Kindle readers.

### EPUB {#EPUB}
```
public static int EPUB
```


EPUB format.

### ODT {#ODT}
```
public static int ODT
```


ODF Text Document.

### OTT {#OTT}
```
public static int OTT
```


ODF Text Document Template.

### TEXT {#TEXT}
```
public static int TEXT
```


Plain Text.

### MARKDOWN {#MARKDOWN}
```
public static int MARKDOWN
```


Markdown text document.

### PDF {#PDF}
```
public static int PDF
```


Pdf document.

### XML {#XML}
```
public static int XML
```


XML document.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Unrecognized format, cannot be loaded by Aspose.Words.

### length {#length}
```
public static int length
```


### getName(int loadFormat) {#getName-int-}
```
public static String getName(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### toString(int loadFormat) {#toString-int-}
```
public static String toString(int loadFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |

**Returns:**
java.lang.String
### fromName(String loadFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String loadFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormatName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
