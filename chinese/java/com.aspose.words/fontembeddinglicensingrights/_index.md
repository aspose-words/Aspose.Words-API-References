---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words for Java"
description: "表示在 Java 中字体的嵌入许可权。"
type: docs
weight: 321
url: /zh/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

表示字体的嵌入许可权。

 **Remarks:** 

欲了解更多信息，请访问 Microsoft Typography 门户上的 [ OpenType specification section ][OpenType specification section]。

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


[OpenType specification section]: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype
## 方法

| 方法 | 描述 |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | 指示 “仅位图嵌入” 限制。 |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | 使用权限。 |
| [getNoSubsetting()](#getNoSubsetting) | 指示 “不子集化” 限制。 |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


指示 “仅位图嵌入” 限制。

 **Remarks:** 

当此位被设置时，仅可嵌入字体中包含的位图。轮廓数据不能嵌入。如果字体中没有可用的位图，则该字体被视为不可嵌入，嵌入服务将失败。其他嵌入限制也适用。

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

**Returns:**
boolean - 相应的 boolean 值。
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


使用权限。

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

**Returns:**
int - 对应的 int 值。返回值是 [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/) 常量之一。
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


指示 “不子集化” 限制。

 **Remarks:** 

当此标志被设置时，嵌入前必须不对字体进行子集化。其他嵌入限制也适用。

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

**Returns:**
boolean - 相应的 boolean 值。
