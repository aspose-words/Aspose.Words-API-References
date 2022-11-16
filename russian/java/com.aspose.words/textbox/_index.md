---
title: TextBox
second_title: Справочник по API Aspose.Words для Java
description: Определяет атрибуты, определяющие способ отображения текста внутри фигуры.
type: docs
weight: 558
url: /ru/java/com.aspose.words/textbox/
---

**Наследование:**
java.lang.Object
```
public class TextBox
```

Определяет атрибуты, определяющие способ отображения текста внутри фигуры.

 Чтобы узнать больше, посетите**Working with Shapes** документальная статья.

 Использовать[Shape.getTextBox()](../../com.aspose.words/shape\#getTextBox--) свойство для доступа к текстовым свойствам фигуры. Вы не создаете экземпляры[TextBox](../../com.aspose.words/textbox) класс напрямую.
## Методы

| Метод | Описание |
| --- | --- |
| [breakForwardLink()](#breakForwardLink--) | Разрывает ссылку на следующий TextBox. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getFitShapeToText()](#getFitShapeToText--) | Определяет, будет ли Microsoft Word увеличивать фигуру до размера текста. |
| [getInternalMarginBottom()](#getInternalMarginBottom--) | Указывает внутреннее нижнее поле в пунктах для фигуры. |
| [getInternalMarginLeft()](#getInternalMarginLeft--) | Указывает внутреннее левое поле в пунктах для фигуры. |
| [getInternalMarginRight()](#getInternalMarginRight--) | Указывает внутреннее правое поле в точках для фигуры. |
| [getInternalMarginTop()](#getInternalMarginTop--) | Указывает внутреннее верхнее поле в пунктах для фигуры. |
| [getLayoutFlow()](#getLayoutFlow--) | Определяет поток макета текста в фигуре. |
| [getNext()](#getNext--) | Получает TextBox, представляющий следующий TextBox в последовательности фигур. |
| [getParent()](#getParent--) | Получает родительскую фигуру для TextBox. |
| [getPrevious()](#getPrevious--) | Возвращает TextBox, представляющий предыдущий TextBox в последовательности фигур. |
| [getTextBoxWrapMode()](#getTextBoxWrapMode--) | Определяет, как текст обтекает фигуру. |
| [getVerticalAnchor()](#getVerticalAnchor--) | Задает вертикальное выравнивание текста внутри фигуры. |
| [hashCode()](#hashCode--) |  |
| [isValidLinkTarget(TextBox target)](#isValidLinkTarget-com.aspose.words.TextBox-) | Определяет, может ли это TextBox быть связано с целевым TextBox. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFitShapeToText(boolean value)](#setFitShapeToText-boolean-) | Определяет, будет ли Microsoft Word увеличивать фигуру до размера текста. |
| [setInternalMarginBottom(double value)](#setInternalMarginBottom-double-) | Указывает внутреннее нижнее поле в пунктах для фигуры. |
| [setInternalMarginLeft(double value)](#setInternalMarginLeft-double-) | Указывает внутреннее левое поле в пунктах для фигуры. |
| [setInternalMarginRight(double value)](#setInternalMarginRight-double-) | Указывает внутреннее правое поле в точках для фигуры. |
| [setInternalMarginTop(double value)](#setInternalMarginTop-double-) | Указывает внутреннее верхнее поле в пунктах для фигуры. |
| [setLayoutFlow(int value)](#setLayoutFlow-int-) | Определяет поток макета текста в фигуре. |
| [setNext(TextBox value)](#setNext-com.aspose.words.TextBox-) | Задает TextBox, представляющий следующий TextBox в последовательности фигур. |
| [setTextBoxWrapMode(int value)](#setTextBoxWrapMode-int-) | Определяет, как текст обтекает фигуру. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | Задает вертикальное выравнивание текста внутри фигуры. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### breakForwardLink() {#breakForwardLink--}
```
public void breakForwardLink()
```


Разрывает ссылку на следующий TextBox. BreakForwardLink() не разрывает все остальные ссылки в текущей последовательности фигур. Например: последовательность 1-2-3-4 и BreakForwardLink во втором текстовом поле создадут две последовательности 1-2, 3-4.

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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getFitShapeToText() {#getFitShapeToText--}
```
public boolean getFitShapeToText()
```


Определяет, будет ли Microsoft Word увеличивать фигуру до размера текста.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getInternalMarginBottom() {#getInternalMarginBottom--}
```
public double getInternalMarginBottom()
```


Указывает внутреннее нижнее поле в пунктах для фигуры.

Значение по умолчанию — 1/20 дюйма.

**Возвращает:**
double - соответствующее двойное значение.
### getInternalMarginLeft() {#getInternalMarginLeft--}
```
public double getInternalMarginLeft()
```


Указывает внутреннее левое поле в пунктах для фигуры.

Значение по умолчанию — 1/10 дюйма.

**Возвращает:**
double - соответствующее двойное значение.
### getInternalMarginRight() {#getInternalMarginRight--}
```
public double getInternalMarginRight()
```


Указывает внутреннее правое поле в точках для фигуры.

Значение по умолчанию — 1/10 дюйма.

**Возвращает:**
double - соответствующее двойное значение.
### getInternalMarginTop() {#getInternalMarginTop--}
```
public double getInternalMarginTop()
```


Указывает внутреннее верхнее поле в пунктах для фигуры.

Значение по умолчанию — 1/20 дюйма.

**Возвращает:**
double - соответствующее двойное значение.
### getLayoutFlow() {#getLayoutFlow--}
```
public int getLayoutFlow()
```


Определяет поток макета текста в фигуре.

 Значение по умолчанию[LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow\#HORIZONTAL).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[LayoutFlow](../../com.aspose.words/layoutflow) константы.
### getNext() {#getNext--}
```
public TextBox getNext()
```


Получает TextBox, представляющий следующий TextBox в последовательности фигур.

**Возвращает:**
[TextBox](../../com.aspose.words/textbox) - TextBox, представляющий следующий TextBox в последовательности фигур.
### getParent() {#getParent--}
```
public Shape getParent()
```


Получает родительскую фигуру для TextBox.

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Родительская форма для TextBox.
### getPrevious() {#getPrevious--}
```
public TextBox getPrevious()
```


Возвращает TextBox, представляющий предыдущий TextBox в последовательности фигур.

**Возвращает:**
[TextBox](../../com.aspose.words/textbox) - TextBox, представляющий предыдущий TextBox в последовательности фигур.
### getTextBoxWrapMode() {#getTextBoxWrapMode--}
```
public int getTextBoxWrapMode()
```


Определяет, как текст обтекает фигуру.

 Значение по умолчанию[TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode\#SQUARE).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[TextBoxWrapMode](../../com.aspose.words/textboxwrapmode) константы.
### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


Задает вертикальное выравнивание текста внутри фигуры.

 Значение по умолчанию[TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor\#TOP).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[TextBoxAnchor](../../com.aspose.words/textboxanchor) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isValidLinkTarget(TextBox target) {#isValidLinkTarget-com.aspose.words.TextBox-}
```
public boolean isValidLinkTarget(TextBox target)
```


Определяет, может ли это TextBox быть связано с целевым TextBox.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| target | [TextBox](../../com.aspose.words/textbox) |  |

**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setFitShapeToText(boolean value) {#setFitShapeToText-boolean-}
```
public void setFitShapeToText(boolean value)
```


Определяет, будет ли Microsoft Word увеличивать фигуру до размера текста.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setInternalMarginBottom(double value) {#setInternalMarginBottom-double-}
```
public void setInternalMarginBottom(double value)
```


Указывает внутреннее нижнее поле в пунктах для фигуры.

Значение по умолчанию — 1/20 дюйма.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setInternalMarginLeft(double value) {#setInternalMarginLeft-double-}
```
public void setInternalMarginLeft(double value)
```


Указывает внутреннее левое поле в пунктах для фигуры.

Значение по умолчанию — 1/10 дюйма.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setInternalMarginRight(double value) {#setInternalMarginRight-double-}
```
public void setInternalMarginRight(double value)
```


Указывает внутреннее правое поле в точках для фигуры.

Значение по умолчанию — 1/10 дюйма.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setInternalMarginTop(double value) {#setInternalMarginTop-double-}
```
public void setInternalMarginTop(double value)
```


Указывает внутреннее верхнее поле в пунктах для фигуры.

Значение по умолчанию — 1/20 дюйма.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setLayoutFlow(int value) {#setLayoutFlow-int-}
```
public void setLayoutFlow(int value)
```


Определяет поток макета текста в фигуре.

 Значение по умолчанию[LayoutFlow.HORIZONTAL](../../com.aspose.words/layoutflow\#HORIZONTAL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[LayoutFlow](../../com.aspose.words/layoutflow) константы. |

### setNext(TextBox value) {#setNext-com.aspose.words.TextBox-}
```
public void setNext(TextBox value)
```


Задает TextBox, представляющий следующий TextBox в последовательности фигур.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [TextBox](../../com.aspose.words/textbox) | TextBox, представляющий следующий TextBox в последовательности фигур. |

### setTextBoxWrapMode(int value) {#setTextBoxWrapMode-int-}
```
public void setTextBoxWrapMode(int value)
```


Определяет, как текст обтекает фигуру.

 Значение по умолчанию[TextBoxWrapMode.SQUARE](../../com.aspose.words/textboxwrapmode\#SQUARE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[TextBoxWrapMode](../../com.aspose.words/textboxwrapmode) константы. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


Задает вертикальное выравнивание текста внутри фигуры.

 Значение по умолчанию[TextBoxAnchor.TOP](../../com.aspose.words/textboxanchor\#TOP).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[TextBoxAnchor](../../com.aspose.words/textboxanchor) константы. |

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
