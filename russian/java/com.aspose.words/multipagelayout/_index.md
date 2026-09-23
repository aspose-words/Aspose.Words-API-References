---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words для Java"
description: "Определяет макет для рендеринга нескольких страниц в один вывод в Java."
type: docs
weight: 472
url: /ru/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Определяет макет для рендеринга нескольких страниц в один вывод.

 **Remarks:** 

Используйте один из статических методов‑фабрик для создания конфигурации макета.

 **Examples:** 

Показывает, как сохранить документ в изображение JPG с настройками макета нескольких страниц.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getBackColor()](#getBackColor) | Возвращает цвет фона вывода. |
| [getBorderColor()](#getBorderColor) | Возвращает цвет границы страниц. |
| [getBorderWidth()](#getBorderWidth) | Возвращает ширину границы страниц. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Создаёт макет, в котором страницы рендерятся слева направо, сверху вниз, в сетке с указанным числом столбцов. |
| [horizontal(float horizontalGap)](#horizontal-float) | Создаёт макет, в котором все указанные страницы рендерятся горизонтально рядом, слева направо, в едином выводе. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Устанавливает цвет фона вывода. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Устанавливает цвет границы страниц. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Устанавливает ширину границы страниц. |
| [singlePage()](#singlePage) | Создаёт макет, который рендерит только первую из указанных страниц. |
| [tiffFrames()](#tiffFrames) | Создаёт макет, где каждая страница рендерится как отдельный кадр в многокадровом изображении TIFF. |
| [vertical(float verticalGap)](#vertical-float) | Создаёт макет, где все указанные страницы рендерятся вертикально одна под другой в едином выводе. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Возвращает цвет фона вывода. По умолчанию java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color — Цвет фона вывода.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Возвращает цвет границы страниц. По умолчанию java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color — Цвет границы страниц.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Получает ширину границы страниц. По умолчанию 0.

**Returns:**
float - Ширина границы страниц.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Создаёт макет, в котором страницы рендерятся слева направо, сверху вниз, в сетке с указанным числом столбцов.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| колонки | int | Количество колонок в макете. Должно быть больше нуля. |
| horizontalGap | float | Горизонтальный зазор между колонками в пунктах. |
| verticalGap | float | Вертикальный зазор между строками в пунктах. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Создаёт макет, в котором все указанные страницы рендерятся горизонтально рядом, слева направо, в едином выводе.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| horizontalGap | float | Горизонтальный зазор между страницами в пунктах. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Устанавливает цвет фона вывода. По умолчанию java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет фона вывода. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Устанавливает цвет границы страниц. По умолчанию java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет границы страниц. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Устанавливает ширину границы страниц. По умолчанию 0.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | float | Ширина границы страниц. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Создаёт макет, который рендерит только первую из указанных страниц.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Создаёт макет, в котором каждая страница отображается как отдельный кадр в многокадровом TIFF‑изображении. Применяется только к форматам изображений TIFF.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Создаёт макет, где все указанные страницы рендерятся вертикально одна под другой в едином выводе.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| verticalGap | float | Вертикальный зазор между страницами в пунктах. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
