---
title: CheckGrammarOptions
linktitle: CheckGrammarOptions
second_title: Aspose.Words for Java
description: Allows to specify various options while checking grammar of a document using AI in Java.
type: docs
weight: 99
url: /java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

Allows to specify various options while checking grammar of a document using AI.
## Methods

| Method | Description |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | Allows to specify either AI will try to improve stylistics of the text being proofed. |
| [getMakeRevisions()](#getMakeRevisions) | Allows to specify either final or revised document to be returned with proofed text. |
| [getPreserveFormatting()](#getPreserveFormatting) | Allows to specify either [IAiModelText.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/iaimodeltext/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) will try to preserve layout and formatting of the original document, or not. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | Allows to specify either AI will try to improve stylistics of the text being proofed. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | Allows to specify either final or revised document to be returned with proofed text. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | Allows to specify either [IAiModelText.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/iaimodeltext/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) will try to preserve layout and formatting of the original document, or not. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


Allows to specify either AI will try to improve stylistics of the text being proofed. Default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


Allows to specify either final or revised document to be returned with proofed text. Default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


Allows to specify either [IAiModelText.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/iaimodeltext/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) will try to preserve layout and formatting of the original document, or not. Default value is  true .

 **Remarks:** 

When the option is set to  false , the quality of grammar checking is higher than when this option is set to  true . However, the original formatting of the text is not preserved in this case.

**Returns:**
boolean - The corresponding  boolean  value.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


Allows to specify either AI will try to improve stylistics of the text being proofed. Default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


Allows to specify either final or revised document to be returned with proofed text. Default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


Allows to specify either [IAiModelText.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/iaimodeltext/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) will try to preserve layout and formatting of the original document, or not. Default value is  true .

 **Remarks:** 

When the option is set to  false , the quality of grammar checking is higher than when this option is set to  true . However, the original formatting of the text is not preserved in this case.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

