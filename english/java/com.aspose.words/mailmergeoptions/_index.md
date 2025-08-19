---
title: MailMergeOptions
linktitle: MailMergeOptions
second_title: Aspose.Words for Java
description: Represents options for the mail merge functionality in Java.
type: docs
weight: 438
url: /java/com.aspose.words/mailmergeoptions/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeOptions
```

Represents options for the mail merge functionality.

 **Examples:** 

Shows how to do mail merge operation for a single record.

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.2.docx", SaveFormat.DOCX, fieldNames, fieldValues);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.3.docx", SaveFormat.DOCX, fieldNames, fieldValues, options);
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [MailMergeOptions()](#MailMergeOptions) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getCleanupOptions()](#getCleanupOptions) | Gets a set of flags that specify what items should be removed during mail merge. |
| [getCleanupParagraphsWithPunctuationMarks()](#getCleanupParagraphsWithPunctuationMarks) | Gets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |
| [getMergeDuplicateRegions()](#getMergeDuplicateRegions) | Gets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [getMergeWholeDocument()](#getMergeWholeDocument) | Gets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [getPreserveUnusedTags()](#getPreserveUnusedTags) | Gets a value indicating whether the unused "mustache" tags should be preserved. |
| [getRegionEndTag()](#getRegionEndTag) | Gets a mail merge region end tag. |
| [getRegionStartTag()](#getRegionStartTag) | Gets a mail merge region start tag. |
| [getRestartListsAtEachSection()](#getRestartListsAtEachSection) | Gets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [getRetainFirstSectionStart()](#getRetainFirstSectionStart) | Gets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [getTrimWhitespaces()](#getTrimWhitespaces) | Gets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [getUnconditionalMergeFieldsAndRegions()](#getUnconditionalMergeFieldsAndRegions) | Gets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [getUseNonMergeFields()](#getUseNonMergeFields) | When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags. |
| [getUseWholeParagraphAsRegion()](#getUseWholeParagraphAsRegion) | Gets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |
| [setCleanupOptions(int value)](#setCleanupOptions-int) | Sets a set of flags that specify what items should be removed during mail merge. |
| [setCleanupParagraphsWithPunctuationMarks(boolean value)](#setCleanupParagraphsWithPunctuationMarks-boolean) | Sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |
| [setMergeDuplicateRegions(boolean value)](#setMergeDuplicateRegions-boolean) | Sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |
| [setMergeWholeDocument(boolean value)](#setMergeWholeDocument-boolean) | Sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions. |
| [setPreserveUnusedTags(boolean value)](#setPreserveUnusedTags-boolean) | Sets a value indicating whether the unused "mustache" tags should be preserved. |
| [setRegionEndTag(String value)](#setRegionEndTag-java.lang.String) | Sets a mail merge region end tag. |
| [setRegionStartTag(String value)](#setRegionStartTag-java.lang.String) | Sets a mail merge region start tag. |
| [setRestartListsAtEachSection(boolean value)](#setRestartListsAtEachSection-boolean) | Sets a value indicating whether lists are restarted at each section after executing of a mail merge. |
| [setRetainFirstSectionStart(boolean value)](#setRetainFirstSectionStart-boolean) | Sets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |
| [setTrimWhitespaces(boolean value)](#setTrimWhitespaces-boolean) | Sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |
| [setUnconditionalMergeFieldsAndRegions(boolean value)](#setUnconditionalMergeFieldsAndRegions-boolean) | Sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |
| [setUseNonMergeFields(boolean value)](#setUseNonMergeFields-boolean) | When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags. |
| [setUseWholeParagraphAsRegion(boolean value)](#setUseWholeParagraphAsRegion-boolean) | Sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |
### MailMergeOptions() {#MailMergeOptions}
```
public MailMergeOptions()
```


Initializes a new instance of this class.

### getCleanupOptions() {#getCleanupOptions}
```
public int getCleanupOptions()
```


Gets a set of flags that specify what items should be removed during mail merge.

**Returns:**
int - A set of flags that specify what items should be removed during mail merge. The returned value is a bitwise combination of [MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions/) constants.
### getCleanupParagraphsWithPunctuationMarks() {#getCleanupParagraphsWithPunctuationMarks}
```
public boolean getCleanupParagraphsWithPunctuationMarks()
```


Gets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.

 **Remarks:** 

The default value is  true .

Here is the complete list of cleanable punctuation marks:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  ¡
 *  ¿

**Returns:**
boolean - A value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.
### getMergeDuplicateRegions() {#getMergeDuplicateRegions}
```
public boolean getMergeDuplicateRegions()
```


Gets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.

 **Remarks:** 

The default value is  false .

**Returns:**
boolean - A value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.
### getMergeWholeDocument() {#getMergeWholeDocument}
```
public boolean getMergeWholeDocument()
```


Gets a value indicating whether fields in whole document are updated while executing of a mail merge with regions.

 **Remarks:** 

The default value is  false .

**Returns:**
boolean - A value indicating whether fields in whole document are updated while executing of a mail merge with regions.
### getPreserveUnusedTags() {#getPreserveUnusedTags}
```
public boolean getPreserveUnusedTags()
```


Gets a value indicating whether the unused "mustache" tags should be preserved.

 **Remarks:** 

The default value is  false .

**Returns:**
boolean - A value indicating whether the unused "mustache" tags should be preserved.
### getRegionEndTag() {#getRegionEndTag}
```
public String getRegionEndTag()
```


Gets a mail merge region end tag.

**Returns:**
java.lang.String - A mail merge region end tag.
### getRegionStartTag() {#getRegionStartTag}
```
public String getRegionStartTag()
```


Gets a mail merge region start tag.

**Returns:**
java.lang.String - A mail merge region start tag.
### getRestartListsAtEachSection() {#getRestartListsAtEachSection}
```
public boolean getRestartListsAtEachSection()
```


Gets a value indicating whether lists are restarted at each section after executing of a mail merge.

 **Remarks:** 

The default value is  true .

**Returns:**
boolean - A value indicating whether lists are restarted at each section after executing of a mail merge.
### getRetainFirstSectionStart() {#getRetainFirstSectionStart}
```
public boolean getRetainFirstSectionStart()
```


Gets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.

 **Remarks:** 

The default value is  true .

**Returns:**
boolean - A value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.
### getTrimWhitespaces() {#getTrimWhitespaces}
```
public boolean getTrimWhitespaces()
```


Gets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to do mail merge operation for a single record.

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.2.docx", SaveFormat.DOCX, fieldNames, fieldValues);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.3.docx", SaveFormat.DOCX, fieldNames, fieldValues, options);
 
```

**Returns:**
boolean - A value indicating whether trailing and leading whitespaces are trimmed from mail merge values.
### getUnconditionalMergeFieldsAndRegions() {#getUnconditionalMergeFieldsAndRegions}
```
public boolean getUnconditionalMergeFieldsAndRegions()
```


Gets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.

 **Remarks:** 

The default value is  false .

**Returns:**
boolean - A value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.
### getUseNonMergeFields() {#getUseNonMergeFields}
```
public boolean getUseNonMergeFields()
```


When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags.

 **Remarks:** 

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [getUseNonMergeFields()](../../com.aspose.words/mailmergeoptions/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmergeoptions/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "\{FieldName\}" ""

Also, when [getUseNonMergeFields()](../../com.aspose.words/mailmergeoptions/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmergeoptions/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into text tags "\{\{fieldName\}\}". These are not fields, but just text tags.

**Returns:**
boolean - The corresponding  boolean  value.
### getUseWholeParagraphAsRegion() {#getUseWholeParagraphAsRegion}
```
public boolean getUseWholeParagraphAsRegion()
```


Gets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.

 **Remarks:** 

The default value is  true .

**Returns:**
boolean - A value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.
### setCleanupOptions(int value) {#setCleanupOptions-int}
```
public void setCleanupOptions(int value)
```


Sets a set of flags that specify what items should be removed during mail merge.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A set of flags that specify what items should be removed during mail merge. The value must be a bitwise combination of [MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions/) constants. |

### setCleanupParagraphsWithPunctuationMarks(boolean value) {#setCleanupParagraphsWithPunctuationMarks-boolean}
```
public void setCleanupParagraphsWithPunctuationMarks(boolean value)
```


Sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified.

 **Remarks:** 

The default value is  true .

Here is the complete list of cleanable punctuation marks:

 *  !
 *  ,
 *  .
 *  :
 *  ;
 *  ?
 *  ¡
 *  ¿

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the [MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-PARAGRAPHS) option is specified. |

### setMergeDuplicateRegions(boolean value) {#setMergeDuplicateRegions-boolean}
```
public void setMergeDuplicateRegions(boolean value)
```


Sets a value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one.

 **Remarks:** 

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether all of the document mail merge regions with the name of a data source should be merged while executing of a mail merge with regions against the data source or just the first one. |

### setMergeWholeDocument(boolean value) {#setMergeWholeDocument-boolean}
```
public void setMergeWholeDocument(boolean value)
```


Sets a value indicating whether fields in whole document are updated while executing of a mail merge with regions.

 **Remarks:** 

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether fields in whole document are updated while executing of a mail merge with regions. |

### setPreserveUnusedTags(boolean value) {#setPreserveUnusedTags-boolean}
```
public void setPreserveUnusedTags(boolean value)
```


Sets a value indicating whether the unused "mustache" tags should be preserved.

 **Remarks:** 

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the unused "mustache" tags should be preserved. |

### setRegionEndTag(String value) {#setRegionEndTag-java.lang.String}
```
public void setRegionEndTag(String value)
```


Sets a mail merge region end tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A mail merge region end tag. |

### setRegionStartTag(String value) {#setRegionStartTag-java.lang.String}
```
public void setRegionStartTag(String value)
```


Sets a mail merge region start tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A mail merge region start tag. |

### setRestartListsAtEachSection(boolean value) {#setRestartListsAtEachSection-boolean}
```
public void setRestartListsAtEachSection(boolean value)
```


Sets a value indicating whether lists are restarted at each section after executing of a mail merge.

 **Remarks:** 

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether lists are restarted at each section after executing of a mail merge. |

### setRetainFirstSectionStart(boolean value) {#setRetainFirstSectionStart-boolean}
```
public void setRetainFirstSectionStart(boolean value)
```


Sets a value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour.

 **Remarks:** 

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether the section start of the first document section and its copies for subsequent data source rows are retained during mail merge or updated according to MS Word behaviour. |

### setTrimWhitespaces(boolean value) {#setTrimWhitespaces-boolean}
```
public void setTrimWhitespaces(boolean value)
```


Sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to do mail merge operation for a single record.

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.2.docx", SaveFormat.DOCX, fieldNames, fieldValues);
 MailMergeOptions options = new MailMergeOptions();
 options.setTrimWhitespaces(true);
 MailMerger.execute(doc, getArtifactsDir() + "LowCode.MailMerge.3.docx", SaveFormat.DOCX, fieldNames, fieldValues, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether trailing and leading whitespaces are trimmed from mail merge values. |

### setUnconditionalMergeFieldsAndRegions(boolean value) {#setUnconditionalMergeFieldsAndRegions-boolean}
```
public void setUnconditionalMergeFieldsAndRegions(boolean value)
```


Sets a value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition.

 **Remarks:** 

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether merge fields and merge regions are merged regardless of the parent IF field's condition. |

### setUseNonMergeFields(boolean value) {#setUseNonMergeFields-boolean}
```
public void setUseNonMergeFields(boolean value)
```


When  true , specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "\{\{fieldName\}\}" tags.

 **Remarks:** 

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [getUseNonMergeFields()](../../com.aspose.words/mailmergeoptions/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmergeoptions/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "\{FieldName\}" ""

Also, when [getUseNonMergeFields()](../../com.aspose.words/mailmergeoptions/\#getUseNonMergeFields) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmergeoptions/\#setUseNonMergeFields-boolean) is set to  true , Aspose.Words will perform mail merge into text tags "\{\{fieldName\}\}". These are not fields, but just text tags.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUseWholeParagraphAsRegion(boolean value) {#setUseWholeParagraphAsRegion-boolean}
```
public void setUseWholeParagraphAsRegion(boolean value)
```


Sets a value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region.

 **Remarks:** 

The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether whole paragraph with **TableStart** or **TableEnd** field or particular range between **TableStart** and **TableEnd** fields should be included into mail merge region. |

