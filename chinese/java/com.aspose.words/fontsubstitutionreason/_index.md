---
title: "FontSubstitutionReason"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words for Java"
description: "指定 Java 中字体替换的原因。"
type: docs
weight: 335
url: /zh/java/com.aspose.words/fontsubstitutionreason/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionReason
```

指定字体替换的原因。

 **Examples:** 

展示如何获取有关字体替换的附加信息。

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 WarningInfoCollection callback = new WarningInfoCollection();
 doc.setWarningCallback(callback);

 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Arial", "Arvo", "Slab");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarnings.pdf");

 FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback.get(0);
 Assert.assertEquals(WarningSource.LAYOUT, warningInfo.getSource());
 Assert.assertEquals(WarningType.FONT_SUBSTITUTION, warningInfo.getWarningType());
 Assert.assertEquals(FontSubstitutionReason.TABLE_SUBSTITUTION_RULE, warningInfo.getReason());
 Assert.assertEquals("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo.getDescription());
 Assert.assertTrue(warningInfo.getRequestedBold());
 Assert.assertFalse(warningInfo.getRequestedItalic());
 Assert.assertEquals("Arial", warningInfo.getRequestedFamilyName());
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [ALTERNATIVE_NAME](#ALTERNATIVE-NAME) | 通过文档中的替代名称进行字体替换。 |
| [DEFAULT_FONT_SUBSTITUTION_RULE](#DEFAULT-FONT-SUBSTITUTION-RULE) | 通过默认字体规则进行字体替换。 |
| [FIRST_AVAILABLE_FONT](#FIRST-AVAILABLE-FONT) | 使用第一个可用字体进行字体替换。 |
| [FONT_CONFIG_SUBSTITUTION_RULE](#FONT-CONFIG-SUBSTITUTION-RULE) | 通过字体配置规则进行字体替换。 |
| [FONT_INFO_SUBSTITUTION_RULE](#FONT-INFO-SUBSTITUTION-RULE) | 通过字体信息规则进行字体替换。 |
| [FONT_NAME_SUBSTITUTION_RULE](#FONT-NAME-SUBSTITUTION-RULE) | 通过字体名称规则进行字体替换。 |
| [TABLE_SUBSTITUTION_RULE](#TABLE-SUBSTITUTION-RULE) | 通过表规则进行字体替换。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String fontSubstitutionReasonName)](#fromName-java.lang.String) |  |
| [getName(int fontSubstitutionReason)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSubstitutionReason)](#toString-int) |  |
### ALTERNATIVE_NAME {#ALTERNATIVE-NAME}
```
public static int ALTERNATIVE_NAME
```


通过文档中的替代名称进行字体替换。

### DEFAULT_FONT_SUBSTITUTION_RULE {#DEFAULT-FONT-SUBSTITUTION-RULE}
```
public static int DEFAULT_FONT_SUBSTITUTION_RULE
```


通过默认字体规则进行字体替换。

### FIRST_AVAILABLE_FONT {#FIRST-AVAILABLE-FONT}
```
public static int FIRST_AVAILABLE_FONT
```


使用第一个可用字体进行字体替换。

### FONT_CONFIG_SUBSTITUTION_RULE {#FONT-CONFIG-SUBSTITUTION-RULE}
```
public static int FONT_CONFIG_SUBSTITUTION_RULE
```


通过字体配置规则进行字体替换。

### FONT_INFO_SUBSTITUTION_RULE {#FONT-INFO-SUBSTITUTION-RULE}
```
public static int FONT_INFO_SUBSTITUTION_RULE
```


通过字体信息规则进行字体替换。

### FONT_NAME_SUBSTITUTION_RULE {#FONT-NAME-SUBSTITUTION-RULE}
```
public static int FONT_NAME_SUBSTITUTION_RULE
```


通过字体名称规则进行字体替换。

### TABLE_SUBSTITUTION_RULE {#TABLE-SUBSTITUTION-RULE}
```
public static int TABLE_SUBSTITUTION_RULE
```


通过表规则进行字体替换。

### length {#length}
```
public static int length
```


### fromName(String fontSubstitutionReasonName) {#fromName-java.lang.String}
```
public static int fromName(String fontSubstitutionReasonName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontSubstitutionReasonName | java.lang.String |  |

**Returns:**
int
### getName(int fontSubstitutionReason) {#getName-int}
```
public static String getName(int fontSubstitutionReason)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontSubstitutionReason) {#toString-int}
```
public static String toString(int fontSubstitutionReason)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
