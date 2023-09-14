---
title: ImportFormatMode
linktitle: ImportFormatMode
second_title: Aspose.Words for Java
description: Specifies how formatting is merged when importing content from another document in Java.
type: docs
weight: 361
url: /java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Specifies how formatting is merged when importing content from another document.

 **Remarks:** 

When you copy nodes from one document to another, this option specifies how formatting is resolved when both documents have a style with the same name, but different formatting.

The formatting is resolved as follows:

1.  Built-in styles are matched using their locale independent style identifier. User defined styles are matched using case-sensitive style name.
2.  If a matching style is not found in the destination document, the style (and all styles referenced by it) are copied into the destination document and the imported nodes are updated to reference the new style.
3.  If a matching style already exists in the destination document, what happens depends on the  importFormatMode  parameter passed to **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** as described below.

When using the [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) option, if a matching style already exists in the destination document, the style is not copied and the imported nodes are updated to reference the existing style.

The drawback of using [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) is that the imported text might look different in the destination document comparing to the source document. For example, the "Heading 1" style in the source document uses Arial 16pt font and the "Heading 1" style in the destination document uses Times New Roman 14pt font. When importing text of "Heading 1" style with no other direct formatting, it will appear as Times New Roman 14pt font in the destination document.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

The drawback of using [KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) is that if you perform several imports, you could end up with many styles in the destination document and that could make using consistent style formatting in Microsoft Word difficult for this document.

Using [KEEP\_DIFFERENT\_STYLES](../../com.aspose.words/importformatmode/\#KEEP-DIFFERENT-STYLES) option allows to reuse destination styles if the formatting they provide is identical to the styles in the source document. If the style in destination document is different from the source then it is imported.

 **Examples:** 

Shows how to insert a document into another document.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Fields

| Field | Description |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Only copy styles that are different from those in the source document. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Copy all required styles to the destination document, generate unique style names if needed. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Use the destination document styles and copy new styles. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Only copy styles that are different from those in the source document.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Copy all required styles to the destination document, generate unique style names if needed.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Use the destination document styles and copy new styles. This is the default option.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
