---
title: CellFormat
second_title: Справочник по API Aspose.Words для Java
description: Представляет все форматирование для ячейки таблицы.
type: docs
weight: 50
url: /ru/java/com.aspose.words/cellformat/
---

**Наследование:**
java.lang.Object
```
public class CellFormat
```

Представляет все форматирование для ячейки таблицы.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Восстанавливает форматирование ячеек по умолчанию. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [getBorders()](#getBorders--) | Получает коллекцию границ ячейки. |
| [getBottomPadding()](#getBottomPadding--) | Получает количество места (в пунктах), которое нужно добавить под содержимым ячейки. |
| [getClass()](#getClass--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getFitText()](#getFitText--) | Если true, текст помещается в ячейку, сжимая каждый абзац до ширины ячейки. |
| [getHorizontalMerge()](#getHorizontalMerge--) | Указывает, как ячейка объединяется по горизонтали с другими ячейками в строке. |
| [getLeftPadding()](#getLeftPadding--) | Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячейки. |
| [getOrientation()](#getOrientation--) | Получает ориентацию текста в ячейке таблицы. |
| [getPreferredWidth()](#getPreferredWidth--) | Получает предпочтительную ширину ячейки. |
| [getRightPadding()](#getRightPadding--) | Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячейки. |
| [getShading()](#getShading--) | Возвращает объект Shading, который ссылается на форматирование заливки для ячейки. |
| [getTopPadding()](#getTopPadding--) | Получает количество места (в пунктах), которое нужно добавить над содержимым ячейки. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Получает вертикальное выравнивание текста в ячейке. |
| [getVerticalMerge()](#getVerticalMerge--) | Указывает, как ячейка объединяется с другими ячейками по вертикали. |
| [getWidth()](#getWidth--) | Получает ширину ячейки в пунктах. |
| [getWrapText()](#getWrapText--) | Если true, оберните текст для ячейки. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Устанавливает количество места (в пунктах) для добавления под содержимым ячейки. |
| [setFitText(boolean value)](#setFitText-boolean-) | Если true, текст помещается в ячейку, сжимая каждый абзац до ширины ячейки. |
| [setHorizontalMerge(int value)](#setHorizontalMerge-int-) | Указывает, как ячейка объединяется по горизонтали с другими ячейками в строке. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Устанавливает количество места (в пунктах) для добавления слева от содержимого ячейки. |
| [setOrientation(int value)](#setOrientation-int-) | Задает ориентацию текста в ячейке таблицы. |
| [setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)](#setPaddings-double-double-double-double-) | Устанавливает количество места (в пунктах), которое добавляется слева/сверху/справа/снизу содержимого ячейки. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | Устанавливает предпочтительную ширину ячейки. |
| [setRightPadding(double value)](#setRightPadding-double-) | Устанавливает количество места (в пунктах) для добавления справа от содержимого ячейки. |
| [setTopPadding(double value)](#setTopPadding-double-) | Устанавливает количество места (в пунктах), которое нужно добавить над содержимым ячейки. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Устанавливает вертикальное выравнивание текста в ячейке. |
| [setVerticalMerge(int value)](#setVerticalMerge-int-) | Указывает, как ячейка объединяется с другими ячейками по вертикали. |
| [setWidth(double value)](#setWidth-double-) | Получает ширину ячейки в пунктах. |
| [setWrapText(boolean value)](#setWrapText-boolean-) | Если true, оберните текст для ячейки. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Восстанавливает форматирование ячеек по умолчанию. Не изменяет ширину ячейки.

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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ ячейки.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Коллекция границ ячейки.
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Получает количество места (в пунктах), которое нужно добавить под содержимым ячейки.

**Возвращает:**
double - количество места (в пунктах), которое нужно добавить под содержимым ячейки.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getFitText() {#getFitText--}
```
public boolean getFitText()
```


Если true, текст помещается в ячейку, сжимая каждый абзац до ширины ячейки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getHorizontalMerge() {#getHorizontalMerge--}
```
public int getHorizontalMerge()
```


Указывает, как ячейка объединяется по горизонтали с другими ячейками в строке.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[CellMerge](../../com.aspose.words/cellmerge) константы.
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячейки.

**Возвращает:**
double - Количество места (в пунктах) для добавления слева от содержимого ячейки.
### getOrientation() {#getOrientation--}
```
public int getOrientation()
```


Получает ориентацию текста в ячейке таблицы.

**Возвращает:**
 int - Ориентация текста в ячейке таблицы. Возвращаемое значение является одним из[TextOrientation](../../com.aspose.words/textorientation) константы.
### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


Получает предпочтительную ширину ячейки.

Предпочтительная ширина (наряду с параметром таблицы «Автоподгонка») определяет, как фактическая ширина ячейки рассчитывается алгоритмом компоновки таблицы. Макет таблицы может быть выполнен Aspose.Words при сохранении документа или Microsoft Word при отображении документа.

Предпочтительная ширина может быть указана в пунктах или процентах. Предпочтительная ширина также может быть указана как «авто», что означает, что предпочтительная ширина не указана.

 Значение по умолчанию[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Возвращает:**
[PreferredWidth](../../com.aspose.words/preferredwidth) - Предпочтительная ширина ячейки.
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячейки.

**Возвращает:**
double - Количество места (в пунктах), которое нужно добавить справа от содержимого ячейки.
### getShading() {#getShading--}
```
public Shading getShading()
```


Возвращает объект Shading, который ссылается на форматирование заливки для ячейки.

**Возвращает:**
[Shading](../../com.aspose.words/shading) - Объект Shading, который ссылается на форматирование заливки для ячейки.
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Получает количество места (в пунктах), которое нужно добавить над содержимым ячейки.

**Возвращает:**
double - количество места (в пунктах), которое нужно добавить над содержимым ячейки.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Получает вертикальное выравнивание текста в ячейке.

**Возвращает:**
 int - Вертикальное выравнивание текста в ячейке. Возвращаемое значение является одним из[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment) константы.
### getVerticalMerge() {#getVerticalMerge--}
```
public int getVerticalMerge()
```


Указывает, как ячейка объединяется с другими ячейками по вертикали.

Ячейки могут быть объединены по вертикали только в том случае, если их левая и правая границы идентичны.

При объединении ячеек по вертикали области отображения объединенных ячеек объединяются. Консолидированная область используется для отображения содержимого первой вертикально объединенной ячейки, а все остальные вертикально объединенные ячейки должны быть пустыми.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[CellMerge](../../com.aspose.words/cellmerge) константы.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Получает ширину ячейки в пунктах.

Ширина рассчитывается Aspose.Words при загрузке и сохранении документа. В настоящее время поддерживаются не все комбинации свойств таблицы, ячейки и документа. Возвращаемое значение может быть неточным для некоторых документов. Она может не точно совпадать с шириной ячейки, рассчитанной MS Word при открытии документа в MS Word.

Задавать это свойство не рекомендуется. Нет никакой гарантии, что ячейка действительно будет иметь заданную ширину. Ширина может быть скорректирована для размещения содержимого ячеек в макете таблицы с автоматическим подбором. Ячейки в других строках могут иметь конфликтующие настройки ширины. Размер таблицы можно изменить, чтобы она поместилась в контейнер или соответствовала настройкам ширины таблицы. Рассмотрите возможность использования[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) для установки ширины ячейки. Установка этого свойства устанавливает[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) неявно, начиная с версии 15.8.

**Возвращает:**
double - Ширина ячейки в пунктах.
### getWrapText() {#getWrapText--}
```
public boolean getWrapText()
```


Если true, оберните текст для ячейки.

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




### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления под содержимым ячейки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить под содержимым ячейки. |

### setFitText(boolean value) {#setFitText-boolean-}
```
public void setFitText(boolean value)
```


Если true, текст помещается в ячейку, сжимая каждый абзац до ширины ячейки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setHorizontalMerge(int value) {#setHorizontalMerge-int-}
```
public void setHorizontalMerge(int value)
```


Указывает, как ячейка объединяется по горизонтали с другими ячейками в строке.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[CellMerge](../../com.aspose.words/cellmerge) константы. |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления слева от содержимого ячейки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить слева от содержимого ячейки. |

### setOrientation(int value) {#setOrientation-int-}
```
public void setOrientation(int value)
```


Задает ориентацию текста в ячейке таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Ориентация текста в ячейке таблицы. Значение должно быть одним из[TextOrientation](../../com.aspose.words/textorientation) константы. |

### setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding) {#setPaddings-double-double-double-double-}
```
public void setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


Устанавливает количество места (в пунктах), которое добавляется слева/сверху/справа/снизу содержимого ячейки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| leftPadding | double |  |
| topPadding | double |  |
| rightPadding | double |  |
| bottomPadding | double |  |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


Устанавливает предпочтительную ширину ячейки.

Предпочтительная ширина (наряду с параметром таблицы «Автоподгонка») определяет, как фактическая ширина ячейки рассчитывается алгоритмом компоновки таблицы. Макет таблицы может быть выполнен Aspose.Words при сохранении документа или Microsoft Word при отображении документа.

Предпочтительная ширина может быть указана в пунктах или процентах. Предпочтительная ширина также может быть указана как «авто», что означает, что предпочтительная ширина не указана.

 Значение по умолчанию[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | Предпочтительная ширина ячейки. |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления справа от содержимого ячейки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить справа от содержимого ячейки. |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Устанавливает количество места (в пунктах), которое нужно добавить над содержимым ячейки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить над содержимым ячейки. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


Устанавливает вертикальное выравнивание текста в ячейке.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Вертикальное выравнивание текста в ячейке. Значение должно быть одним из[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment) константы. |

### setVerticalMerge(int value) {#setVerticalMerge-int-}
```
public void setVerticalMerge(int value)
```


Указывает, как ячейка объединяется с другими ячейками по вертикали.

Ячейки могут быть объединены по вертикали только в том случае, если их левая и правая границы идентичны.

При объединении ячеек по вертикали области отображения объединенных ячеек объединяются. Консолидированная область используется для отображения содержимого первой вертикально объединенной ячейки, а все остальные вертикально объединенные ячейки должны быть пустыми.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[CellMerge](../../com.aspose.words/cellmerge) константы. |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


Получает ширину ячейки в пунктах.

Ширина рассчитывается Aspose.Words при загрузке и сохранении документа. В настоящее время поддерживаются не все комбинации свойств таблицы, ячейки и документа. Возвращаемое значение может быть неточным для некоторых документов. Она может не точно совпадать с шириной ячейки, рассчитанной MS Word при открытии документа в MS Word.

Задавать это свойство не рекомендуется. Нет никакой гарантии, что ячейка действительно будет иметь заданную ширину. Ширина может быть скорректирована для размещения содержимого ячеек в макете таблицы с автоматическим подбором. Ячейки в других строках могут иметь конфликтующие настройки ширины. Размер таблицы можно изменить, чтобы она поместилась в контейнер или соответствовала настройкам ширины таблицы. Рассмотрите возможность использования[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) для установки ширины ячейки. Установка этого свойства устанавливает[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) неявно, начиная с версии 15.8.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Ширина ячейки в пунктах. |

### setWrapText(boolean value) {#setWrapText-boolean-}
```
public void setWrapText(boolean value)
```


Если true, оберните текст для ячейки.

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
