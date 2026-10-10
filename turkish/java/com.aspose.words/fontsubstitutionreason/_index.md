---
title: "FontSubstitutionReason"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words Java için"
description: "Java'da yazı tipi ikamesinin nedenini belirtir."
type: docs
weight: 335
url: /tr/java/com.aspose.words/fontsubstitutionreason/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionReason
```

Yazı tipi ikamesinin nedenini belirtir.

 **Examples:** 

Yazı tipi ikamesi hakkında ek bilgi nasıl alınacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ALTERNATIVE_NAME](#ALTERNATIVE-NAME) | Belgeden alternatif adla yazı tipi ikamesi. |
| [DEFAULT_FONT_SUBSTITUTION_RULE](#DEFAULT-FONT-SUBSTITUTION-RULE) | Varsayılan yazı tipi kuralı ile yazı tipi ikamesi. |
| [FIRST_AVAILABLE_FONT](#FIRST-AVAILABLE-FONT) | İlk kullanılabilir yazı tipiyle yazı tipi ikamesi. |
| [FONT_CONFIG_SUBSTITUTION_RULE](#FONT-CONFIG-SUBSTITUTION-RULE) | Yazı tipi yapılandırma kuralı ile yazı tipi ikamesi. |
| [FONT_INFO_SUBSTITUTION_RULE](#FONT-INFO-SUBSTITUTION-RULE) | Yazı tipi bilgisi kuralı ile yazı tipi ikamesi. |
| [FONT_NAME_SUBSTITUTION_RULE](#FONT-NAME-SUBSTITUTION-RULE) | Yazı tipi adı kuralı ile yazı tipi ikamesi. |
| [TABLE_SUBSTITUTION_RULE](#TABLE-SUBSTITUTION-RULE) | Tablo kuralı ile yazı tipi ikamesi. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fontSubstitutionReasonName)](#fromName-java.lang.String) |  |
| [getName(int fontSubstitutionReason)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSubstitutionReason)](#toString-int) |  |
### ALTERNATIVE_NAME {#ALTERNATIVE-NAME}
```
public static int ALTERNATIVE_NAME
```


Belgeden alternatif adla yazı tipi ikamesi.

### DEFAULT_FONT_SUBSTITUTION_RULE {#DEFAULT-FONT-SUBSTITUTION-RULE}
```
public static int DEFAULT_FONT_SUBSTITUTION_RULE
```


Varsayılan yazı tipi kuralı ile yazı tipi ikamesi.

### FIRST_AVAILABLE_FONT {#FIRST-AVAILABLE-FONT}
```
public static int FIRST_AVAILABLE_FONT
```


İlk kullanılabilir yazı tipiyle yazı tipi ikamesi.

### FONT_CONFIG_SUBSTITUTION_RULE {#FONT-CONFIG-SUBSTITUTION-RULE}
```
public static int FONT_CONFIG_SUBSTITUTION_RULE
```


Yazı tipi yapılandırma kuralı ile yazı tipi ikamesi.

### FONT_INFO_SUBSTITUTION_RULE {#FONT-INFO-SUBSTITUTION-RULE}
```
public static int FONT_INFO_SUBSTITUTION_RULE
```


Yazı tipi bilgisi kuralı ile yazı tipi ikamesi.

### FONT_NAME_SUBSTITUTION_RULE {#FONT-NAME-SUBSTITUTION-RULE}
```
public static int FONT_NAME_SUBSTITUTION_RULE
```


Yazı tipi adı kuralı ile yazı tipi ikamesi.

### TABLE_SUBSTITUTION_RULE {#TABLE-SUBSTITUTION-RULE}
```
public static int TABLE_SUBSTITUTION_RULE
```


Tablo kuralı ile yazı tipi ikamesi.

### length {#length}
```
public static int length
```


### fromName(String fontSubstitutionReasonName) {#fromName-java.lang.String}
```
public static int fromName(String fontSubstitutionReasonName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontSubstitutionReasonName | java.lang.String |  |

**Returns:**
int
### getName(int fontSubstitutionReason) {#getName-int}
```
public static String getName(int fontSubstitutionReason)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
