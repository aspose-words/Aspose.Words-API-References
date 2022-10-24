---
title: PdfPermissions
second_title: Aspose.Words for Java API Reference
description: Specifies the operations that are allowed to a user on an encrypted PDF document.
type: docs
weight: 460
url: /java/com.aspose.words/pdfpermissions/
---

**Inheritance:**
java.lang.Object
```
public class PdfPermissions
```

Specifies the operations that are allowed to a user on an encrypted PDF document.
## Fields

| Field | Description |
| --- | --- |
| [DISALLOW_ALL](#DISALLOW-ALL) | Disallows all operations on the PDF document. |
| [ALLOW_ALL](#ALLOW-ALL) | Allows all operations on the PDF document. |
| [CONTENT_COPY](#CONTENT-COPY) | Copy or otherwise extract text and graphics from the document by operations other than that controlled by [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Extract text and graphics (in support of accessibility to users with disabilities or for other purposes). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) | Modify the contents of the document by operations other than those controlled by [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions\#FILL-IN), and [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions\#DOCUMENT-ASSEMBLY). |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) | Add or modify text annotations, fill in interactive form fields, and, if [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) is also set, create or modify interactive form fields (including signature fields). |
| [FILL_IN](#FILL-IN) | Fill in existing interactive form fields (including signature fields), even if [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) is clear. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) | Assemble the document (insert, rotate, or delete pages and create document outline items or thumbnail images), even if [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) is clear. |
| [PRINTING](#PRINTING) | Print the document (possibly not at the highest quality level, depending on whether [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions\#HIGH-RESOLUTION-PRINTING) is also set). |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Print the document to a representation from which a faithful digital copy of the PDF content could be generated, based on an implementation-dependent algorithm. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfPermissions)](#getName-int-) |  |
| [getNames(int pdfPermissions)](#getNames-int-) |  |
| [toString(int pdfPermissions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set-) |  |
| [getValues()](#getValues--) |  |
### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


Disallows all operations on the PDF document. This is the default value.

### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Allows all operations on the PDF document.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


Copy or otherwise extract text and graphics from the document by operations other than that controlled by [CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Extract text and graphics (in support of accessibility to users with disabilities or for other purposes).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


Modify the contents of the document by operations other than those controlled by [MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions\#FILL-IN), and [DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions\#DOCUMENT-ASSEMBLY).

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


Add or modify text annotations, fill in interactive form fields, and, if [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) is also set, create or modify interactive form fields (including signature fields).

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


Fill in existing interactive form fields (including signature fields), even if [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) is clear.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


Assemble the document (insert, rotate, or delete pages and create document outline items or thumbnail images), even if [MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) is clear.

### PRINTING {#PRINTING}
```
public static int PRINTING
```


Print the document (possibly not at the highest quality level, depending on whether [HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions\#HIGH-RESOLUTION-PRINTING) is also set).

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Print the document to a representation from which a faithful digital copy of the PDF content could be generated, based on an implementation-dependent algorithm. When this flag is clear (and [PRINTING](../../com.aspose.words/pdfpermissions\#PRINTING) is set), printing shall be limited to a low-level representation of the appearance, possibly of degraded quality.

### length {#length}
```
public static int length
```


### getName(int pdfPermissions) {#getName-int-}
```
public static String getName(int pdfPermissions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int-}
```
public static Set getNames(int pdfPermissions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.util.Set
### toString(int pdfPermissions) {#toString-int-}
```
public static String toString(int pdfPermissions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPermissions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### fromName(String pdfPermissionsName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfPermissionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
