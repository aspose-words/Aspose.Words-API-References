---
title: "FontPitch"
linktitle: "FontPitch"
second_title: "Aspose.Words для Java"
description: "Представляет шаг шрифта в Java."
type: docs
weight: 330
url: /ru/java/com.aspose.words/fontpitch/
---

**Inheritance:**
java.lang.Object
```
public class FontPitch
```

Представляет шаг шрифта.

 **Remarks:** 

Шаг указывает, фиксирован ли шрифт, пропорционально распределён или использует настройку по умолчанию.

 **Examples:** 

Показывает, как получить доступ и вывести детали каждого шрифта в документе.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Указывает, что информация о шаге шрифта недоступна. |
| [FIXED](#FIXED) | Указывает, что это шрифт фиксированной ширины. |
| [VARIABLE](#VARIABLE) | Указывает, что это шрифт пропорциональной ширины. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fontPitchName)](#fromName-java.lang.String) |  |
| [getName(int fontPitch)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontPitch)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Указывает, что информация о шаге шрифта недоступна.

### FIXED {#FIXED}
```
public static int FIXED
```


Указывает, что это шрифт фиксированной ширины.

### VARIABLE {#VARIABLE}
```
public static int VARIABLE
```


Указывает, что это шрифт пропорциональной ширины.

### length {#length}
```
public static int length
```


### fromName(String fontPitchName) {#fromName-java.lang.String}
```
public static int fromName(String fontPitchName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPitchName | java.lang.String |  |

**Returns:**
int
### getName(int fontPitch) {#getName-int}
```
public static String getName(int fontPitch)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontPitch) {#toString-int}
```
public static String toString(int fontPitch)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
