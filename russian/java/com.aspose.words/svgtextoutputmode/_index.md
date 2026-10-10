---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words для Java"
description: "Позволяет указать, как текст внутри документа должен отображаться при сохранении в формате SVG в Java."
type: docs
weight: 650
url: /ru/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Позволяет указать, как текст внутри документа должен отображаться при сохранении в формате SVG.

 **Examples:** 

Показывает, как имитировать свойства изображений при конвертации документа .docx в .svg.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Configure the SvgSaveOptions object to save with no page borders or selectable text.
 SvgSaveOptions options = new SvgSaveOptions();
 {
     options.setFitToViewPort(true);
     options.setShowPageBorder(false);
     options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);
 }

 doc.save(getArtifactsDir() + "SvgSaveOptions.SaveLikeImage.svg", options);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Текст отрисовывается с использованием кривых. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | Для отрисовки текста используются шрифты SVG. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Для отрисовки текста используются шрифты, установленные на целевой машине. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Текст отрисовывается с использованием кривых. Обратите внимание, выделение текста не будет работать, если вы используете эту опцию.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


Для отрисовки текста используются шрифты SVG. Обратите внимание, не все браузеры поддерживают шрифты SVG.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Для отрисовки текста используются шрифты, установленные на целевой машине. Обратите внимание, если некоторые шрифты, использованные в документе, недоступны на целевой машине, документ может выглядеть иначе.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int svgTextOutputMode) {#toString-int}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
