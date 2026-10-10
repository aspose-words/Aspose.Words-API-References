---
title: "FontSubstitutionReason"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words для Java"
description: "Указывает причину замены шрифта в Java."
type: docs
weight: 335
url: /ru/java/com.aspose.words/fontsubstitutionreason/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionReason
```

Указывает причину замены шрифта.

 **Examples:** 

Показывает, как получить дополнительную информацию о замене шрифтов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ALTERNATIVE_NAME](#ALTERNATIVE-NAME) | Замена шрифта по альтернативному имени из документа. |
| [DEFAULT_FONT_SUBSTITUTION_RULE](#DEFAULT-FONT-SUBSTITUTION-RULE) | Замена шрифта по правилу шрифта по умолчанию. |
| [FIRST_AVAILABLE_FONT](#FIRST-AVAILABLE-FONT) | Замена шрифта на первый доступный шрифт. |
| [FONT_CONFIG_SUBSTITUTION_RULE](#FONT-CONFIG-SUBSTITUTION-RULE) | Замена шрифта по правилу конфигурации шрифта. |
| [FONT_INFO_SUBSTITUTION_RULE](#FONT-INFO-SUBSTITUTION-RULE) | Замена шрифта по правилу информации о шрифте. |
| [FONT_NAME_SUBSTITUTION_RULE](#FONT-NAME-SUBSTITUTION-RULE) | Замена шрифта по правилу имени шрифта. |
| [TABLE_SUBSTITUTION_RULE](#TABLE-SUBSTITUTION-RULE) | Замена шрифта по правилу таблицы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fontSubstitutionReasonName)](#fromName-java.lang.String) |  |
| [getName(int fontSubstitutionReason)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontSubstitutionReason)](#toString-int) |  |
### ALTERNATIVE_NAME {#ALTERNATIVE-NAME}
```
public static int ALTERNATIVE_NAME
```


Замена шрифта по альтернативному имени из документа.

### DEFAULT_FONT_SUBSTITUTION_RULE {#DEFAULT-FONT-SUBSTITUTION-RULE}
```
public static int DEFAULT_FONT_SUBSTITUTION_RULE
```


Замена шрифта по правилу шрифта по умолчанию.

### FIRST_AVAILABLE_FONT {#FIRST-AVAILABLE-FONT}
```
public static int FIRST_AVAILABLE_FONT
```


Замена шрифта на первый доступный шрифт.

### FONT_CONFIG_SUBSTITUTION_RULE {#FONT-CONFIG-SUBSTITUTION-RULE}
```
public static int FONT_CONFIG_SUBSTITUTION_RULE
```


Замена шрифта по правилу конфигурации шрифта.

### FONT_INFO_SUBSTITUTION_RULE {#FONT-INFO-SUBSTITUTION-RULE}
```
public static int FONT_INFO_SUBSTITUTION_RULE
```


Замена шрифта по правилу информации о шрифте.

### FONT_NAME_SUBSTITUTION_RULE {#FONT-NAME-SUBSTITUTION-RULE}
```
public static int FONT_NAME_SUBSTITUTION_RULE
```


Замена шрифта по правилу имени шрифта.

### TABLE_SUBSTITUTION_RULE {#TABLE-SUBSTITUTION-RULE}
```
public static int TABLE_SUBSTITUTION_RULE
```


Замена шрифта по правилу таблицы.

### length {#length}
```
public static int length
```


### fromName(String fontSubstitutionReasonName) {#fromName-java.lang.String}
```
public static int fromName(String fontSubstitutionReasonName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontSubstitutionReasonName | java.lang.String |  |

**Returns:**
int
### getName(int fontSubstitutionReason) {#getName-int}
```
public static String getName(int fontSubstitutionReason)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontSubstitutionReason | int |  |

**Returns:**
java.lang.String
