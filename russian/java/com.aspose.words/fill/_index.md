---
title: Fill
second_title: Справочник по API Aspose.Words для Java
description: Представляет форматирование заливки для объекта.
type: docs
weight: 267
url: /ru/java/com.aspose.words/fill/
---

**Наследование:**
java.lang.Object
```
public class Fill
```

Представляет форматирование заливки для объекта.

 Чтобы узнать больше, посетите**Working with Graphic Elements** документальная статья.

 Использовать[ShapeBase.getFill()](../../com.aspose.words/shapebase\#getFill--) или же[Font.getFill()](../../com.aspose.words/font\#getFill--) свойство для доступа к свойствам заливки объекта. Вы не создаете экземпляры[Fill](../../com.aspose.words/fill) класс напрямую.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBackColor()](#getBackColor--) | Получает объект Color, представляющий цвет фона для заливки. |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает объект Color, представляющий цвет переднего плана для заливки. |
| [getFillType()](#getFillType--) | Получает тип заполнения. |
| [getForeColor()](#getForeColor--) | Получает объект Color, представляющий цвет переднего плана для заливки. |
| [getGradientAngle()](#getGradientAngle--) | Получает угол градиентной заливки. |
| [getGradientStops()](#getGradientStops--) |  Получает коллекцию[GradientStop](../../com.aspose.words/gradientstop) объекты для заливки. |
| [getGradientStyle()](#getGradientStyle--) |  Получает стиль градиента[GradientStyle](../../com.aspose.words/gradientstyle) для заливки. |
| [getGradientVariant()](#getGradientVariant--) |  Получает градиентный вариант[GradientVariant](../../com.aspose.words/gradientvariant) для заливки. |
| [getImageBytes()](#getImageBytes--) | Получает необработанные байты текстуры или узора заливки. |
| [getOn()](#getOn--) | Получает значение true, если форматирование, примененное к этому экземпляру, видимо. |
| [getOpacity()](#getOpacity--) | Получает степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). |
| [getPattern()](#getPattern--) | Получает[PatternType](../../com.aspose.words/patterntype) для заливки. |
| [getPresetTexture()](#getPresetTexture--) | Получает[PresetTexture](../../com.aspose.words/presettexture) для заливки. |
| [getRotateWithObject()](#getRotateWithObject--) | Получает, вращается ли заливка с указанным объектом. |
| [getTextureAlignment()](#getTextureAlignment--) | Получает выравнивание для заливки текстурой плитки. |
| [getTransparency()](#getTransparency--) | Получает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). |
| [getVisible()](#getVisible--) | Получает значение true, если форматирование, примененное к этому экземпляру, видимо. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [oneColorGradient(int style, int variant, double degree)](#oneColorGradient-int-int-double-) |  |
| [oneColorGradient(Color color, int style, int variant, double degree)](#oneColorGradient-java.awt.Color-int-int-double-) |  |
| [patterned(int patternType)](#patterned-int-) |  |
| [patterned(int patternType, Color foreColor, Color backColor)](#patterned-int-java.awt.Color-java.awt.Color-) |  |
| [presetTextured(int presetTexture)](#presetTextured-int-) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color-) | Задает объект Color, представляющий цвет фона для заливки. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Задает объект Color, представляющий цвет переднего плана для заливки. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color-) | Задает объект Color, представляющий цвет переднего плана для заливки. |
| [setGradientAngle(double value)](#setGradientAngle-double-) | Устанавливает угол градиентной заливки. |
| [setImage(byte[] imageBytes)](#setImage-byte---) | Изменяет тип заливки на одно изображение. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream-) |  |
| [setImage(String fileName)](#setImage-java.lang.String-) | Изменяет тип заливки на одно изображение. |
| [setOn(boolean value)](#setOn-boolean-) | Устанавливает значение, которое является истинным, если форматирование, примененное к этому экземпляру, видимо. |
| [setOpacity(double value)](#setOpacity-double-) | Задает степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). |
| [setRotateWithObject(boolean value)](#setRotateWithObject-boolean-) | Устанавливает, будет ли заливка вращаться вместе с указанным объектом. |
| [setTextureAlignment(int value)](#setTextureAlignment-int-) | Устанавливает выравнивание для заливки текстурой плитки. |
| [setTransparency(double value)](#setTransparency-double-) | Задает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). |
| [setVisible(boolean value)](#setVisible-boolean-) | Устанавливает значение, которое является истинным, если форматирование, примененное к этому экземпляру, видимо. |
| [solid()](#solid--) | Устанавливает заливку однородным цветом. |
| [solid(Color color)](#solid-java.awt.Color-) | Устанавливает заливку заданным однородным цветом. |
| [toString()](#toString--) |  |
| [twoColorGradient(int style, int variant)](#twoColorGradient-int-int-) |  |
| [twoColorGradient(Color color1, Color color2, int style, int variant)](#twoColorGradient-java.awt.Color-java.awt.Color-int-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getBackColor() {#getBackColor--}
```
public Color getBackColor()
```


Получает объект Color, представляющий цвет фона для заливки.

**Возвращает:**
java.awt.Color — объект Color, представляющий цвет фона для заливки.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColor() {#getColor--}
```
public Color getColor()
```


Получает объект Color, представляющий цвет переднего плана для заливки.

**Возвращает:**
java.awt.Color — объект Color, представляющий цвет переднего плана для заливки.
### getFillType() {#getFillType--}
```
public int getFillType()
```


Получает тип заполнения.

**Возвращает:**
 int - тип заполнения. Возвращаемое значение является одним из[FillType](../../com.aspose.words/filltype) константы.
### getForeColor() {#getForeColor--}
```
public Color getForeColor()
```


Получает объект Color, представляющий цвет переднего плана для заливки.

**Возвращает:**
java.awt.Color — объект Color, представляющий цвет переднего плана для заливки.
### getGradientAngle() {#getGradientAngle--}
```
public double getGradientAngle()
```


Получает угол градиентной заливки.

**Возвращает:**
double - Угол градиентной заливки.
### getGradientStops() {#getGradientStops--}
```
public GradientStopCollection getGradientStops()
```


 Получает коллекцию[GradientStop](../../com.aspose.words/gradientstop) объекты для заливки.

**Возвращает:**
[GradientStopCollection](../../com.aspose.words/gradientstopcollection) - Коллекция[GradientStop](../../com.aspose.words/gradientstop) объекты для заливки.
### getGradientStyle() {#getGradientStyle--}
```
public int getGradientStyle()
```


 Получает стиль градиента[GradientStyle](../../com.aspose.words/gradientstyle) для заливки.

**Возвращает:**
 int - Стиль градиента[GradientStyle](../../com.aspose.words/gradientstyle) для заливки. Возвращаемое значение является одним из[GradientStyle](../../com.aspose.words/gradientstyle) константы.
### getGradientVariant() {#getGradientVariant--}
```
public int getGradientVariant()
```


 Получает градиентный вариант[GradientVariant](../../com.aspose.words/gradientvariant) для заливки.

**Возвращает:**
 int - градиентный вариант[GradientVariant](../../com.aspose.words/gradientvariant) для заливки. Возвращаемое значение является одним из[GradientVariant](../../com.aspose.words/gradientvariant) константы.
### getImageBytes() {#getImageBytes--}
```
public byte[] getImageBytes()
```


Получает необработанные байты текстуры или узора заливки.

Значение по умолчанию равно нулю.

**Возвращает:**
байт[] — необработанные байты текстуры или узора заливки.
### getOn() {#getOn--}
```
public boolean getOn()
```


Получает значение true, если форматирование, примененное к этому экземпляру, видимо.

**Возвращает:**
boolean — значение, которое истинно, если форматирование, примененное к этому экземпляру, видимо.
### getOpacity() {#getOpacity--}
```
public double getOpacity()
```


 Получает степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). Это свойство противоположно свойству[getTransparency()](../../com.aspose.words/fill\#getTransparency--) / [setTransparency(double)](../../com.aspose.words/fill\#setTransparency-double-).

**Возвращает:**
double — степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная).
### getPattern() {#getPattern--}
```
public int getPattern()
```


Получает[PatternType](../../com.aspose.words/patterntype) для заливки.

**Возвращает:**
 интервал - А[PatternType](../../com.aspose.words/patterntype) для заливки. Возвращаемое значение является одним из[PatternType](../../com.aspose.words/patterntype) константы.
### getPresetTexture() {#getPresetTexture--}
```
public int getPresetTexture()
```


Получает[PresetTexture](../../com.aspose.words/presettexture) для заливки.

**Возвращает:**
 интервал - А[PresetTexture](../../com.aspose.words/presettexture) для заливки. Возвращаемое значение является одним из[PresetTexture](../../com.aspose.words/presettexture) константы.
### getRotateWithObject() {#getRotateWithObject--}
```
public boolean getRotateWithObject()
```


Получает, вращается ли заливка с указанным объектом.

**Возвращает:**
boolean — вращается ли заливка вместе с указанным объектом.
### getTextureAlignment() {#getTextureAlignment--}
```
public int getTextureAlignment()
```


Получает выравнивание для заливки текстурой плитки.

**Возвращает:**
 int — выравнивание для заливки текстурой плитки. Возвращаемое значение является одним из[TextureAlignment](../../com.aspose.words/texturealignment) константы.
### getTransparency() {#getTransparency--}
```
public double getTransparency()
```


Получает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). Это свойство противоположно свойству[getOpacity()](../../com.aspose.words/fill\#getOpacity--) / [setOpacity(double)](../../com.aspose.words/fill\#setOpacity-double-).

**Возвращает:**
double — степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная).
### getVisible() {#getVisible--}
```
public boolean getVisible()
```


Получает значение true, если форматирование, примененное к этому экземпляру, видимо.

**Возвращает:**
boolean — значение, которое истинно, если форматирование, примененное к этому экземпляру, видимо.
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




### oneColorGradient(int style, int variant, double degree) {#oneColorGradient-int-int-double-}
```
public void oneColorGradient(int style, int variant, double degree)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |
| variant | int |  |
| degree | double |  |

### oneColorGradient(Color color, int style, int variant, double degree) {#oneColorGradient-java.awt.Color-int-int-double-}
```
public void oneColorGradient(Color color, int style, int variant, double degree)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| color | java.awt.Color |  |
| style | int |  |
| variant | int |  |
| degree | double |  |

### patterned(int patternType) {#patterned-int-}
```
public void patterned(int patternType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |

### patterned(int patternType, Color foreColor, Color backColor) {#patterned-int-java.awt.Color-java.awt.Color-}
```
public void patterned(int patternType, Color foreColor, Color backColor)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| patternType | int |  |
| foreColor | java.awt.Color |  |
| backColor | java.awt.Color |  |

### presetTextured(int presetTexture) {#presetTextured-int-}
```
public void presetTextured(int presetTexture)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | int |  |

### setBackColor(Color value) {#setBackColor-java.awt.Color-}
```
public void setBackColor(Color value)
```


Задает объект Color, представляющий цвет фона для заливки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Объект Color, представляющий цвет фона для заливки. |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Задает объект Color, представляющий цвет переднего плана для заливки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Объект Color, представляющий цвет переднего плана для заливки. |

### setForeColor(Color value) {#setForeColor-java.awt.Color-}
```
public void setForeColor(Color value)
```


Задает объект Color, представляющий цвет переднего плана для заливки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Объект Color, представляющий цвет переднего плана для заливки. |

### setGradientAngle(double value) {#setGradientAngle-double-}
```
public void setGradientAngle(double value)
```


Устанавливает угол градиентной заливки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Угол градиентной заливки. |

### setImage(byte[] imageBytes) {#setImage-byte---}
```
public void setImage(byte[] imageBytes)
```


Изменяет тип заливки на одно изображение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] | Массив байтов изображения. |

### setImage(InputStream stream) {#setImage-java.io.InputStream-}
```
public void setImage(InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String-}
```
public void setImage(String fileName)
```


Изменяет тип заливки на одно изображение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Путь к файлу изображения. |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```


Устанавливает значение, которое является истинным, если форматирование, примененное к этому экземпляру, видимо.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, которое истинно, если форматирование, примененное к этому экземпляру, видимо. |

### setOpacity(double value) {#setOpacity-double-}
```
public void setOpacity(double value)
```


 Задает степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). Это свойство противоположно свойству[getTransparency()](../../com.aspose.words/fill\#getTransparency--) / [setTransparency(double)](../../com.aspose.words/fill\#setTransparency-double-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Степень непрозрачности указанной заливки в виде значения от 0,0 (прозрачная) до 1,0 (непрозрачная). |

### setRotateWithObject(boolean value) {#setRotateWithObject-boolean-}
```
public void setRotateWithObject(boolean value)
```


Устанавливает, будет ли заливка вращаться вместе с указанным объектом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Вращается ли заливка вместе с указанным объектом. |

### setTextureAlignment(int value) {#setTextureAlignment-int-}
```
public void setTextureAlignment(int value)
```


Устанавливает выравнивание для заливки текстурой плитки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Выравнивание для заливки текстурой плитки. Значение должно быть одним из[TextureAlignment](../../com.aspose.words/texturealignment) константы. |

### setTransparency(double value) {#setTransparency-double-}
```
public void setTransparency(double value)
```


Задает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). Это свойство противоположно свойству[getOpacity()](../../com.aspose.words/fill\#getOpacity--) / [setOpacity(double)](../../com.aspose.words/fill\#setOpacity-double-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная). |

### setVisible(boolean value) {#setVisible-boolean-}
```
public void setVisible(boolean value)
```


Устанавливает значение, которое является истинным, если форматирование, примененное к этому экземпляру, видимо.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, которое истинно, если форматирование, примененное к этому экземпляру, видимо. |

### solid() {#solid--}
```
public void solid()
```


Устанавливает заливку однородным цветом. Используйте этот метод, чтобы преобразовать любую из заливок обратно в сплошную заливку.

### solid(Color color) {#solid-java.awt.Color-}
```
public void solid(Color color)
```


Устанавливает заливку заданным однородным цветом. Используйте этот метод, чтобы преобразовать любую из заливок обратно в сплошную заливку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| color | java.awt.Color |  |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### twoColorGradient(int style, int variant) {#twoColorGradient-int-int-}
```
public void twoColorGradient(int style, int variant)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | int |  |
| variant | int |  |

### twoColorGradient(Color color1, Color color2, int style, int variant) {#twoColorGradient-java.awt.Color-java.awt.Color-int-int-}
```
public void twoColorGradient(Color color1, Color color2, int style, int variant)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| color1 | java.awt.Color |  |
| color2 | java.awt.Color |  |
| style | int |  |
| variant | int |  |

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
