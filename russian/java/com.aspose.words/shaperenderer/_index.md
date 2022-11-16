---
title: ShapeRenderer
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет методы для рендеринга человека или растрового или векторного изображения или объекта Graphics.
type: docs
weight: 520
url: /ru/java/com.aspose.words/shaperenderer/
---

**Наследование:**
java.lang.Object, [com.aspose.words.NodeRendererBase](../../com.aspose.words/noderendererbase)
```
public class ShapeRenderer extends NodeRendererBase
```

 Предоставляет методы для отображения отдельных[Shape](../../com.aspose.words/shape) или же[GroupShape](../../com.aspose.words/groupshape) в растровое или векторное изображение или в объект Graphics.

 Чтобы узнать больше, посетите**Working with Shapes** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ShapeRenderer(ShapeBase shape)](#ShapeRenderer-com.aspose.words.ShapeBase-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float-) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float-) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getBoundsInPoints()](#getBoundsInPoints--) | Получает фактические границы фигуры в точках. |
| [getClass()](#getClass--) |  |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float-) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float-) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints--) | Получает непрозрачные границы фигуры в точках. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float-) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float-) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getSizeInPoints()](#getSizeInPoints--) | Получает фактический размер фигуры в точках. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float-) | Визуализирует форму в объект java.awt.Graphics2D в указанном масштабе. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float-) | Визуализирует фигуру в объект java.awt.Graphics2D заданного размера. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions-) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions-) | Рендерит форму и сохраняет в изображение. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ShapeRenderer(ShapeBase shape) {#ShapeRenderer-com.aspose.words.ShapeBase-}
```
public ShapeRenderer(ShapeBase shape)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| shape | [ShapeBase](../../com.aspose.words/shapebase) | Объект формы DrawinML, который вы хотите визуализировать. |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float-}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 Этот метод преобразует[getBoundsInPoints()](../../com.aspose.words/noderendererbase\#getBoundsInPoints--) в прямоугольник в пикселях.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| dpi | float | Разрешение (горизонтальное и вертикальное) для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Rectangle — Фактическая (отображаемая на странице) ограничивающая рамка фигуры в пикселях.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float-}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 Этот метод преобразует[getBoundsInPoints()](../../com.aspose.words/noderendererbase\#getBoundsInPoints--) в прямоугольник в пикселях.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования точек в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Rectangle — Фактическая (отображаемая на странице) ограничивающая рамка фигуры в пикселях.
### getBoundsInPoints() {#getBoundsInPoints--}
```
public Rectangle2D.Float getBoundsInPoints()
```


Получает фактические границы фигуры в точках.

Это свойство возвращает фактическую (отображаемую на странице) ограничивающую рамку фигуры. Границы учитывают вращение формы (если есть).

**Возвращает:**
java.awt.geom.Rectangle2D.Float — фактические границы фигуры в точках.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float-}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 Этот метод преобразует[getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase\#getOpaqueBoundsInPoints--) в прямоугольник в пикселях, и это полезно, когда вы хотите создать растровое изображение для визуализации фигуры только с непрозрачной частью фигуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| dpi | float | Разрешение для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Rectangle — непрозрачный прямоугольник фигуры в пикселях.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float-}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 Этот метод преобразует[getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase\#getOpaqueBoundsInPoints--) в прямоугольник в пикселях, и это полезно, когда вы хотите создать растровое изображение для визуализации фигуры только с непрозрачной частью фигуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования точек в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Rectangle — непрозрачный прямоугольник фигуры в пикселях.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints--}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


Получает непрозрачные границы фигуры в точках.

Это свойство возвращает непрозрачную (т.е. прозрачные части фигуры игнорируются) ограничивающую рамку фигуры. Границы учитывают вращение формы.

**Возвращает:**
java.awt.geom.Rectangle2D.Float — непрозрачные границы формы в точках.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float-}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 Этот метод преобразует[getSizeInPoints()](../../com.aspose.words/noderendererbase\#getSizeInPoints--) в размер в пикселях, и это полезно, когда вы хотите создать растровое изображение для аккуратного рендеринга формы на растровое изображение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| dpi | float | Разрешение (горизонтальное и вертикальное) для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Dimension — размер фигуры в пикселях.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float-}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 Этот метод преобразует[getSizeInPoints()](../../com.aspose.words/noderendererbase\#getSizeInPoints--) в размер в пикселях, и это полезно, когда вы хотите создать растровое изображение для аккуратного рендеринга формы на растровое изображение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования точек в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Dimension — размер фигуры в пикселях.
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


Получает фактический размер фигуры в точках.

Это свойство возвращает размер фактического (отображаемого на странице) ограничивающего прямоугольника фигуры. Размер учитывает поворот формы (если есть).

**Возвращает:**
java.awt.geom.Point2D.Float — Фактический размер фигуры в пунктах.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float-}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


Визуализирует форму в объект java.awt.Graphics2D в указанном масштабе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| graphics | java.awt.Graphics2D | Объект, на который выполняется рендеринг. |
| x | float | Координата X (в мировых единицах измерения) верхнего левого угла отображаемой фигуры. |
| y | float | Координата Y (в мировых единицах измерения) верхнего левого угла отображаемой фигуры. |
| scale | float | Масштаб рендеринга формы (1.0 — 100%). |

**Возвращает:**
java.awt.geom.Point2D.Float — ширина и высота (в мировых единицах) визуализируемой формы.
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float-}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


Визуализирует фигуру в объект java.awt.Graphics2D заданного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| graphics | java.awt.Graphics2D | Объект, на который выполняется рендеринг. |
| x | float | Координата X (в мировых единицах измерения) верхнего левого угла отображаемой фигуры. |
| y | float | Координата Y (в мировых единицах измерения) верхнего левого угла отображаемой фигуры. |
| width | float | Максимальная ширина (в мировых единицах), которую может занимать отображаемая фигура. |
| height | float | Максимальная высота (в мировых единицах), которую может занимать отображаемая фигура. |

**Возвращает:**
float - Масштаб, который был автоматически рассчитан для визуализируемой формы, чтобы соответствовать указанному размеру.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions-}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions-}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


Рендерит форму и сохраняет в изображение. Преобразует фигуру в изображение и сохраняет в файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл перезаписывается. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) | Указывает параметры, управляющие визуализацией и сохранением фигуры. Может быть нулевым. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
