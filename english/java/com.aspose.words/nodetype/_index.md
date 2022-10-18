---
title: NodeType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 408
url: /java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

A utility class providing constants. Specifies the type of a Word document node.
## Fields

| Field | Description |
| --- | --- |
| [ANY](#ANY) | Indicates all node types. |
| [DOCUMENT](#DOCUMENT) | A [Document](../../com.aspose.words/document) object that, as the root of the document tree, provides access to the entire Word document. |
| [SECTION](#SECTION) | A [Section](../../com.aspose.words/section) object that corresponds to one section in a Word document. |
| [BODY](#BODY) | A [Body](../../com.aspose.words/body) object that contains the main text of a section (main text story). |
| [HEADER_FOOTER](#HEADER-FOOTER) | A [HeaderFooter](../../com.aspose.words/headerfooter) object that contains text of a particular header or footer inside a section. |
| [TABLE](#TABLE) | A [Table](../../com.aspose.words/table) object that represents a table in a Word document. |
| [ROW](#ROW) | A row of a table. |
| [CELL](#CELL) | A cell of a table row. |
| [PARAGRAPH](#PARAGRAPH) | A paragraph of text. |
| [BOOKMARK_START](#BOOKMARK-START) | A beginning of a bookmark marker. |
| [BOOKMARK_END](#BOOKMARK-END) | An end of a bookmark marker. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | A beginning of an editable range. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | An end of an editable range. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | A beginning of an MoveFrom range. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | An end of an MoveFrom range. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | A beginning of an MoveTo range. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | An end of an MoveTo range. |
| [GROUP_SHAPE](#GROUP-SHAPE) | A group of shapes, images, OLE objects or other group shapes. |
| [SHAPE](#SHAPE) | A drawing object, such as an OfficeArt shape, image or an OLE object. |
| [COMMENT](#COMMENT) | A comment in a Word document. |
| [FOOTNOTE](#FOOTNOTE) | A footnote or endnote in a Word document. |
| [RUN](#RUN) | A run of text. |
| [FIELD_START](#FIELD-START) | A special character that designates the start of a Word field. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | A special character that separates the field code from the field result. |
| [FIELD_END](#FIELD-END) | A special character that designates the end of a Word field. |
| [FORM_FIELD](#FORM-FIELD) | A form field. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | A special character that is not one of the more specific special character types. |
| [SMART_TAG](#SMART-TAG) | A smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Allows to define customer-specific information and its means of presentation. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | A start of **ranged** structured document tag which accepts multi-sections content. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | A end of **ranged** structured document tag which accepts multi-sections content. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | A glossary document within the main document. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | A building block within a glossary document (e.g. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | A marker node that represents the start of a commented range. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | A marker node that represents the end of a commented range. |
| [OFFICE_MATH](#OFFICE-MATH) | An Office Math object. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | A subdocument node which is a link to another document. |
| [SYSTEM](#SYSTEM) | Reserved for internal use by Aspose.Words. |
| [NULL](#NULL) | Reserved for internal use by Aspose.Words. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int nodeType)](#getName-int-) |  |
| [toString(int nodeType)](#toString-int-) |  |
| [fromName(String nodeTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### ANY {#ANY}
```
public static int ANY
```


Indicates all node types. Allows to select all children.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


A [Document](../../com.aspose.words/document) object that, as the root of the document tree, provides access to the entire Word document.

A [Document](../../com.aspose.words/document) node can have [Section](../../com.aspose.words/section) nodes.

### SECTION {#SECTION}
```
public static int SECTION
```


A [Section](../../com.aspose.words/section) object that corresponds to one section in a Word document.

A [Section](../../com.aspose.words/section) node can have **Body** and **HeaderFooter** nodes.

### BODY {#BODY}
```
public static int BODY
```


A [Body](../../com.aspose.words/body) object that contains the main text of a section (main text story).

A [Body](../../com.aspose.words/body) node can have [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


A [HeaderFooter](../../com.aspose.words/headerfooter) object that contains text of a particular header or footer inside a section.

A [HeaderFooter](../../com.aspose.words/headerfooter) node can have [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes.

### TABLE {#TABLE}
```
public static int TABLE
```


A [Table](../../com.aspose.words/table) object that represents a table in a Word document.

A [Table](../../com.aspose.words/table) node can have [Row](../../com.aspose.words/row) nodes.

### ROW {#ROW}
```
public static int ROW
```


A row of a table.

A [Row](../../com.aspose.words/row) node can have [Cell](../../com.aspose.words/cell) nodes.

### CELL {#CELL}
```
public static int CELL
```


A cell of a table row.

A [Cell](../../com.aspose.words/cell) node can have [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


A paragraph of text.

A [Paragraph](../../com.aspose.words/paragraph) node is a container for inline level elements [Run](../../com.aspose.words/run), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [Footnote](../../com.aspose.words/footnote), [Comment](../../com.aspose.words/comment), [SpecialChar](../../com.aspose.words/specialchar), as well as [BookmarkStart](../../com.aspose.words/bookmarkstart) and [BookmarkEnd](../../com.aspose.words/bookmarkend).

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


A beginning of a bookmark marker.

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


An end of a bookmark marker.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


A beginning of an editable range.

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


An end of an editable range.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


A beginning of an MoveFrom range.

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


An end of an MoveFrom range.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


A beginning of an MoveTo range.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


An end of an MoveTo range.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


A group of shapes, images, OLE objects or other group shapes.

A [GroupShape](../../com.aspose.words/groupshape) node can contain other [Shape](../../com.aspose.words/shape) and [GroupShape](../../com.aspose.words/groupshape) nodes.

### SHAPE {#SHAPE}
```
public static int SHAPE
```


A drawing object, such as an OfficeArt shape, image or an OLE object.

A [Shape](../../com.aspose.words/shape) node can contain [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


A comment in a Word document.

A [Comment](../../com.aspose.words/comment) node can have [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


A footnote or endnote in a Word document.

A [Footnote](../../com.aspose.words/footnote) node can have [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) nodes.

### RUN {#RUN}
```
public static int RUN
```


A run of text.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


A special character that designates the start of a Word field.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


A special character that separates the field code from the field result.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


A special character that designates the end of a Word field.

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


A form field.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


A special character that is not one of the more specific special character types.

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


A smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Allows to define customer-specific information and its means of presentation.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


A start of **ranged** structured document tag which accepts multi-sections content.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


A end of **ranged** structured document tag which accepts multi-sections content.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


A glossary document within the main document.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


A building block within a glossary document (e.g. glossary document entry).

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


A marker node that represents the start of a commented range.

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


A marker node that represents the end of a commented range.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


An Office Math object. Can be equation, function, matrix or one of other mathematical objects. Can be a collection of mathematical object and also can contain some non-mathematical objects such as runs of text.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


A subdocument node which is a link to another document.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Reserved for internal use by Aspose.Words.

### NULL {#NULL}
```
public static int NULL
```


Reserved for internal use by Aspose.Words.

### length {#length}
```
public static int length
```


### getName(int nodeType) {#getName-int-}
```
public static String getName(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### toString(int nodeType) {#toString-int-}
```
public static String toString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### fromName(String nodeTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
