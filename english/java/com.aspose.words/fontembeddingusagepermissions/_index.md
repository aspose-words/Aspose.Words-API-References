---
title: FontEmbeddingUsagePermissions
linktitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words for Java
description: Represents the font embedding usage permissions in Java.
type: docs
weight: 312
url: /java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

Represents the font embedding usage permissions.

 **Examples:** 

Shows how to get license rights information for embedded fonts (FontInfo).

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [EDITABLE](#EDITABLE) | The font may be embedded, and may be temporarily loaded on other systems. |
| [INSTALLABLE](#INSTALLABLE) | The font may be embedded, and may be permanently installed for use on a remote systems, or for use by other users. |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | The font may be embedded, and may be temporarily loaded on other systems for purposes of viewing or printing the document. |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | The font must not be modified, embedded or exchanged in any manner without first obtaining explicit permission of the legal owner. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


The font may be embedded, and may be temporarily loaded on other systems.

 **Remarks:** 

As with Preview & Print embedding, documents containing Editable fonts may be opened for reading. In addition, editing is permitted, including ability to format new text using the embedded font, and changes may be saved.

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


The font may be embedded, and may be permanently installed for use on a remote systems, or for use by other users.

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


The font may be embedded, and may be temporarily loaded on other systems for purposes of viewing or printing the document.

 **Remarks:** 

Documents containing Preview & Print fonts must be opened \\u201cread-only\\u201d; no edits may be applied to the document.

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


The font must not be modified, embedded or exchanged in any manner without first obtaining explicit permission of the legal owner.

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontEmbeddingUsagePermissions) {#toString-int}
```
public static String toString(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
