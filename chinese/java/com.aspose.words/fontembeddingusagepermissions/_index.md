---
title: "FontEmbeddingUsagePermissions"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words for Java"
description: "表示 Java 中的字体嵌入使用权限。"
type: docs
weight: 322
url: /zh/java/com.aspose.words/fontembeddingusagepermissions/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingUsagePermissions
```

表示字体嵌入使用权限。

 **Examples:** 

展示如何获取嵌入字体（FontInfo）的许可证权利信息。

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
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [EDITABLE](#EDITABLE) | 该字体可以嵌入，并可临时加载到其他系统上。 |
| [INSTALLABLE](#INSTALLABLE) | 该字体可以嵌入，并可永久安装以在远程系统上使用，或供其他用户使用。 |
| [PRINT_AND_PREVIEW](#PRINT-AND-PREVIEW) | 该字体可以嵌入，并可临时加载到其他系统上，以用于查看或打印文档。 |
| [RESTRICTED_LICENSE](#RESTRICTED-LICENSE) | 未经合法所有者明确许可，禁止以任何方式修改、嵌入或交换该字体。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String fontEmbeddingUsagePermissionsName)](#fromName-java.lang.String) |  |
| [getName(int fontEmbeddingUsagePermissions)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontEmbeddingUsagePermissions)](#toString-int) |  |
### EDITABLE {#EDITABLE}
```
public static int EDITABLE
```


该字体可以嵌入，并可临时加载到其他系统上。

 **Remarks:** 

与预览和打印嵌入相同，包含可编辑字体的文档可以以只读方式打开。此外，允许编辑，包括使用嵌入字体格式化新文本，并且可以保存更改。

### INSTALLABLE {#INSTALLABLE}
```
public static int INSTALLABLE
```


该字体可以嵌入，并可永久安装以在远程系统上使用，或供其他用户使用。

### PRINT_AND_PREVIEW {#PRINT-AND-PREVIEW}
```
public static int PRINT_AND_PREVIEW
```


该字体可以嵌入，并可临时加载到其他系统上，以用于查看或打印文档。

 **Remarks:** 

包含 Preview & Print 字体的文档必须以 \u201cread-only\u201d 打开；文档不得进行任何编辑。

### RESTRICTED_LICENSE {#RESTRICTED-LICENSE}
```
public static int RESTRICTED_LICENSE
```


未经合法所有者明确许可，禁止以任何方式修改、嵌入或交换该字体。

### length {#length}
```
public static int length
```


### fromName(String fontEmbeddingUsagePermissionsName) {#fromName-java.lang.String}
```
public static int fromName(String fontEmbeddingUsagePermissionsName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontEmbeddingUsagePermissionsName | java.lang.String |  |

**Returns:**
int
### getName(int fontEmbeddingUsagePermissions) {#getName-int}
```
public static String getName(int fontEmbeddingUsagePermissions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontEmbeddingUsagePermissions | int |  |

**Returns:**
java.lang.String
