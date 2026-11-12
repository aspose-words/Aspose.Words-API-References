---
title: "Ориентация"
linktitle: "Ориентация"
second_title: "Aspose.Words для Java"
description: "Указывает ориентацию страницы в Java."
type: docs
weight: 507
url: /ru/java/com.aspose.words/orientation/
---

**Inheritance:**
java.lang.Object
```
public class Orientation
```

Указывает ориентацию страницы.

 **Examples:** 

Показывает, как применять и отменять настройки разметки страницы для разделов в документе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [LANDSCAPE](#LANDSCAPE) | Ориентация страницы альбомная (широкая и короткая). |
| [PORTRAIT](#PORTRAIT) | Ориентация страницы книжная (узкая и высокая). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String orientationName)](#fromName-java.lang.String) |  |
| [getName(int orientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int orientation)](#toString-int) |  |
### LANDSCAPE {#LANDSCAPE}
```
public static int LANDSCAPE
```


Ориентация страницы альбомная (широкая и короткая).

### PORTRAIT {#PORTRAIT}
```
public static int PORTRAIT
```


Ориентация страницы книжная (узкая и высокая).

### length {#length}
```
public static int length
```


### fromName(String orientationName) {#fromName-java.lang.String}
```
public static int fromName(String orientationName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| orientationName | java.lang.String |  |

**Returns:**
int
### getName(int orientation) {#getName-int}
```
public static String getName(int orientation)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int orientation) {#toString-int}
```
public static String toString(int orientation)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
