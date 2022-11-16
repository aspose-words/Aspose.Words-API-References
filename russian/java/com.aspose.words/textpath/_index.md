---
title: TextPath
second_title: Справочник по API Aspose.Words для Java
description: Определяет текст и форматирование пути к тексту объекта WordArt.
type: docs
weight: 567
url: /ru/java/com.aspose.words/textpath/
---

**Наследование:**
java.lang.Object
```
public class TextPath
```

Определяет текст и форматирование пути к тексту (объекта WordArt).

 Чтобы узнать больше, посетите**Working with Shapes** документальная статья.

 Использовать[Shape.getTextPath()](../../com.aspose.words/shape\#getTextPath--) для доступа к свойствам WordArt фигуры. Вы не создаете экземпляры[TextPath](../../com.aspose.words/textpath) класс напрямую.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBold()](#getBold--) | Истинно, если шрифт отформатирован как полужирный. |
| [getClass()](#getClass--) |  |
| [getFitPath()](#getFitPath--) | Определяет, соответствует ли текст контуру фигуры. |
| [getFitShape()](#getFitShape--) | Определяет, соответствует ли текст ограничивающей рамке фигуры. |
| [getFontFamily()](#getFontFamily--) | Определяет семейство шрифта textpath. |
| [getItalic()](#getItalic--) | Истинно, если шрифт отформатирован как курсив. |
| [getKerning()](#getKerning--) | Определяет, включен ли кернинг. |
| [getOn()](#getOn--) | Определяет, будет ли отображаться текст. |
| [getReverseRows()](#getReverseRows--) | Определяет, является ли порядок расположения строк обратным. |
| [getRotateLetters()](#getRotateLetters--) | Определяет, повернуты ли буквы текста. |
| [getSameLetterHeights()](#getSameLetterHeights--) | Определяет, будут ли все буквы одинаковой высоты независимо от начального регистра. |
| [getShadow()](#getShadow--) | Определяет, применяется ли тень к тексту на текстовом пути. |
| [getSize()](#getSize--) | Определяет размер шрифта в пунктах. |
| [getSmallCaps()](#getSmallCaps--) | Истинно, если шрифт отформатирован как маленькие заглавные буквы. |
| [getSpacing()](#getSpacing--) | Определяет количество интервалов для текста. |
| [getStrikeThrough()](#getStrikeThrough--) | Истинно, если шрифт отформатирован как зачеркнутый текст. |
| [getText()](#getText--) | Определяет текст текстового пути. |
| [getTextPathAlignment()](#getTextPathAlignment--) | Определяет выравнивание текста. |
| [getTrim()](#getTrim--) | Определяет, удаляется ли лишнее пространство над и под текстом. |
| [getUnderline()](#getUnderline--) | Истинно, если шрифт подчеркнут. |
| [getXScale()](#getXScale--) | Определяет, будет ли использоваться прямой текстовый путь вместо контура формы. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBold(boolean value)](#setBold-boolean-) | Истинно, если шрифт отформатирован как полужирный. |
| [setFitPath(boolean value)](#setFitPath-boolean-) | Определяет, соответствует ли текст контуру фигуры. |
| [setFitShape(boolean value)](#setFitShape-boolean-) | Определяет, соответствует ли текст ограничивающей рамке фигуры. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String-) | Определяет семейство шрифта textpath. |
| [setItalic(boolean value)](#setItalic-boolean-) | Истинно, если шрифт отформатирован как курсив. |
| [setKerning(boolean value)](#setKerning-boolean-) | Определяет, включен ли кернинг. |
| [setOn(boolean value)](#setOn-boolean-) | Определяет, будет ли отображаться текст. |
| [setReverseRows(boolean value)](#setReverseRows-boolean-) | Определяет, является ли порядок расположения строк обратным. |
| [setRotateLetters(boolean value)](#setRotateLetters-boolean-) | Определяет, повернуты ли буквы текста. |
| [setSameLetterHeights(boolean value)](#setSameLetterHeights-boolean-) | Определяет, будут ли все буквы одинаковой высоты независимо от начального регистра. |
| [setShadow(boolean value)](#setShadow-boolean-) | Определяет, применяется ли тень к тексту на текстовом пути. |
| [setSize(double value)](#setSize-double-) | Определяет размер шрифта в пунктах. |
| [setSmallCaps(boolean value)](#setSmallCaps-boolean-) | Истинно, если шрифт отформатирован как маленькие заглавные буквы. |
| [setSpacing(double value)](#setSpacing-double-) | Определяет количество интервалов для текста. |
| [setStrikeThrough(boolean value)](#setStrikeThrough-boolean-) | Истинно, если шрифт отформатирован как зачеркнутый текст. |
| [setText(String value)](#setText-java.lang.String-) | Определяет текст текстового пути. |
| [setTextPathAlignment(int value)](#setTextPathAlignment-int-) | Определяет выравнивание текста. |
| [setTrim(boolean value)](#setTrim-boolean-) | Определяет, удаляется ли лишнее пространство над и под текстом. |
| [setUnderline(boolean value)](#setUnderline-boolean-) | Истинно, если шрифт подчеркнут. |
| [setXScale(boolean value)](#setXScale-boolean-) | Определяет, будет ли использоваться прямой текстовый путь вместо контура формы. |
| [toString()](#toString--) |  |
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
### getBold() {#getBold--}
```
public boolean getBold()
```


Истинно, если шрифт отформатирован как полужирный.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getFitPath() {#getFitPath--}
```
public boolean getFitPath()
```


Определяет, соответствует ли текст контуру фигуры.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFitShape() {#getFitShape--}
```
public boolean getFitShape()
```


Определяет, соответствует ли текст ограничивающей рамке фигуры.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFontFamily() {#getFontFamily--}
```
public String getFontFamily()
```


Определяет семейство шрифта textpath.

Значение по умолчанию — Arial.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


Истинно, если шрифт отформатирован как курсив.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getKerning() {#getKerning--}
```
public boolean getKerning()
```


Определяет, включен ли кернинг.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOn() {#getOn--}
```
public boolean getOn()
```


Определяет, будет ли отображаться текст.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getReverseRows() {#getReverseRows--}
```
public boolean getReverseRows()
```


Определяет, является ли порядок расположения строк обратным.

 Значение по умолчанию**false**.

 Если**true**, порядок расположения строк обратный. Этот атрибут используется для вертикального расположения текста.

**Возвращает:**
boolean - соответствующее логическое значение.
### getRotateLetters() {#getRotateLetters--}
```
public boolean getRotateLetters()
```


Определяет, повернуты ли буквы текста.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSameLetterHeights() {#getSameLetterHeights--}
```
public boolean getSameLetterHeights()
```


Определяет, будут ли все буквы одинаковой высоты независимо от начального регистра.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


Определяет, применяется ли тень к тексту на текстовом пути.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSize() {#getSize--}
```
public double getSize()
```


Определяет размер шрифта в пунктах.

Значение по умолчанию — 36.

**Возвращает:**
double - соответствующее двойное значение.
### getSmallCaps() {#getSmallCaps--}
```
public boolean getSmallCaps()
```


Истинно, если шрифт отформатирован как маленькие заглавные буквы.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


Определяет количество интервалов для текста. 1 означает 100%.

Значение по умолчанию — 1.

**Возвращает:**
double - соответствующее двойное значение.
### getStrikeThrough() {#getStrikeThrough--}
```
public boolean getStrikeThrough()
```


Истинно, если шрифт отформатирован как зачеркнутый текст.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getText() {#getText--}
```
public String getText()
```


Определяет текст текстового пути.

Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getTextPathAlignment() {#getTextPathAlignment--}
```
public int getTextPathAlignment()
```


Определяет выравнивание текста.

 Значение по умолчанию[TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment\#CENTER).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[TextPathAlignment](../../com.aspose.words/textpathalignment) константы.
### getTrim() {#getTrim--}
```
public boolean getTrim()
```


Определяет, удаляется ли лишнее пространство над и под текстом.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUnderline() {#getUnderline--}
```
public boolean getUnderline()
```


Истинно, если шрифт подчеркнут.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getXScale() {#getXScale--}
```
public boolean getXScale()
```


Определяет, будет ли использоваться прямой текстовый путь вместо контура формы.

 Значение по умолчанию**false**.

 Если**true**, текст проходит по пути слева направо вдоль значения x нижней границы фигуры.

**Возвращает:**
boolean - соответствующее логическое значение.
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




### setBold(boolean value) {#setBold-boolean-}
```
public void setBold(boolean value)
```


Истинно, если шрифт отформатирован как полужирный.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFitPath(boolean value) {#setFitPath-boolean-}
```
public void setFitPath(boolean value)
```


Определяет, соответствует ли текст контуру фигуры.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFitShape(boolean value) {#setFitShape-boolean-}
```
public void setFitShape(boolean value)
```


Определяет, соответствует ли текст ограничивающей рамке фигуры.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFontFamily(String value) {#setFontFamily-java.lang.String-}
```
public void setFontFamily(String value)
```


Определяет семейство шрифта textpath.

Значение по умолчанию — Arial.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


Истинно, если шрифт отформатирован как курсив.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setKerning(boolean value) {#setKerning-boolean-}
```
public void setKerning(boolean value)
```


Определяет, включен ли кернинг.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOn(boolean value) {#setOn-boolean-}
```
public void setOn(boolean value)
```


Определяет, будет ли отображаться текст.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setReverseRows(boolean value) {#setReverseRows-boolean-}
```
public void setReverseRows(boolean value)
```


Определяет, является ли порядок расположения строк обратным.

 Значение по умолчанию**false**.

 Если**true**, порядок расположения строк обратный. Этот атрибут используется для вертикального расположения текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setRotateLetters(boolean value) {#setRotateLetters-boolean-}
```
public void setRotateLetters(boolean value)
```


Определяет, повернуты ли буквы текста.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSameLetterHeights(boolean value) {#setSameLetterHeights-boolean-}
```
public void setSameLetterHeights(boolean value)
```


Определяет, будут ли все буквы одинаковой высоты независимо от начального регистра.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


Определяет, применяется ли тень к тексту на текстовом пути.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSize(double value) {#setSize-double-}
```
public void setSize(double value)
```


Определяет размер шрифта в пунктах.

Значение по умолчанию — 36.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setSmallCaps(boolean value) {#setSmallCaps-boolean-}
```
public void setSmallCaps(boolean value)
```


Истинно, если шрифт отформатирован как маленькие заглавные буквы.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


Определяет количество интервалов для текста. 1 означает 100%.

Значение по умолчанию — 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setStrikeThrough(boolean value) {#setStrikeThrough-boolean-}
```
public void setStrikeThrough(boolean value)
```


Истинно, если шрифт отформатирован как зачеркнутый текст.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Определяет текст текстового пути.

Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTextPathAlignment(int value) {#setTextPathAlignment-int-}
```
public void setTextPathAlignment(int value)
```


Определяет выравнивание текста.

 Значение по умолчанию[TextPathAlignment.CENTER](../../com.aspose.words/textpathalignment\#CENTER).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[TextPathAlignment](../../com.aspose.words/textpathalignment) константы. |

### setTrim(boolean value) {#setTrim-boolean-}
```
public void setTrim(boolean value)
```


Определяет, удаляется ли лишнее пространство над и под текстом.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUnderline(boolean value) {#setUnderline-boolean-}
```
public void setUnderline(boolean value)
```


Истинно, если шрифт подчеркнут.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setXScale(boolean value) {#setXScale-boolean-}
```
public void setXScale(boolean value)
```


Определяет, будет ли использоваться прямой текстовый путь вместо контура формы.

 Значение по умолчанию**false**.

 Если**true**, текст проходит по пути слева направо вдоль значения x нижней границы фигуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
