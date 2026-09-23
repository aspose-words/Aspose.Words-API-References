---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words для Java"
description: "Представляет семейство шрифтов в Java."
type: docs
weight: 324
url: /ru/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Представляет семейство шрифтов.

 **Remarks:** 

Семейство шрифтов — это набор шрифтов с одинаковой толщиной штриха и характеристиками засечек.

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
| [AUTO](#AUTO) | Указывает общее название семейства. |
| [DECORATIVE](#DECORATIVE) | Указывает декоративный шрифт. |
| [MODERN](#MODERN) | Указывает моноширинный шрифт с засечками или без них. |
| [ROMAN](#ROMAN) | Указывает пропорциональный шрифт с засечками. |
| [SCRIPT](#SCRIPT) | Указывает шрифт, имитирующий рукописный текст; примеры включают Script и Cursive. |
| [SWISS](#SWISS) | Указывает пропорциональный шрифт без засечек. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Указывает общее семейство шрифтов. Это имя используется, когда информация о шрифте отсутствует или не важна. Используется шрифт по умолчанию.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Указывает декоративный шрифт. Примером является Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


Указывает моноширинный шрифт с засечками или без них. Моноширинные шрифты обычно современные; примеры включают Pica, Elite и Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Указывает пропорциональный шрифт с засечками. Примером является Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Указывает шрифт, имитирующий рукописный текст; примеры включают Script и Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


Указывает пропорциональный шрифт без засечек. Примером является Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontFamily) {#toString-int}
```
public static String toString(int fontFamily)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
