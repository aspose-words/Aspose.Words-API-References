---
title: RevisionOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет контролировать, как обрабатываются версии документа в процессе компоновки.
type: docs
weight: 488
url: /ru/java/com.aspose.words/revisionoptions/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

Позволяет контролировать, как обрабатываются версии документа в процессе компоновки.

 Чтобы узнать больше, посетите**Converting to Fixed-page Format** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCommentColor()](#getCommentColor--) | Позволяет указать цвет, который будет использоваться для комментариев. |
| [getDeletedTextColor()](#getDeletedTextColor--) | Позволяет указать цвет, который будет использоваться для удаленного контента.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect--) |  Позволяет указать эффект, который будет применяться к удаленному содержимому.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [getInsertedTextColor()](#getInsertedTextColor--) |  Позволяет указать цвет, который будет использоваться для вставленного содержимого.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect--) |  Позволяет указать эффект, который будет применяться к вставленному содержимому.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit--) | Позволяет указать единицы измерения для комментариев к ревизии. |
| [getMovedFromTextColor()](#getMovedFromTextColor--) |  Позволяет указать цвет, который будет использоваться для областей, из которых было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect--) |  Позволяет указать эффект, который будет применяться к областям, из которых был перемещен контент.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor--) |  Позволяет указать цвет, который будет использоваться для областей, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect--) |  Позволяет указать эффект, который будет применяться к областям, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor--) |  Позволяет указать цвет, который будет использоваться для содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect--) |  Позволяет указать эффект для областей содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) не допускается и вызовет исключение java.lang.IllegalArgumentException. |
| [getRevisionBarsColor()](#getRevisionBarsColor--) | Позволяет указать цвет, который будет использоваться для боковых полос, обозначающих строки документа, содержащие исправленную информацию. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition--) | Получает позицию рендеринга исправлений. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth--) | Получает ширину ревизионных полос в пунктах. |
| [getShowInBalloons()](#getShowInBalloons--) | Позволяет указать, будут ли ревизии отображаться во всплывающих подсказках. |
| [getShowOriginalRevision()](#getShowOriginalRevision--) | Позволяет указать, должен ли отображаться исходный текст вместо исправленного. |
| [getShowRevisionBars()](#getShowRevisionBars--) | Позволяет указать, следует ли отображать полосы изменений рядом со строками, содержащими исправленное содержимое. |
| [getShowRevisionMarks()](#getShowRevisionMarks--) | Позволяет указать, следует ли помечать текст ревизии специальной разметкой форматирования. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCommentColor(int value)](#setCommentColor-int-) | Позволяет указать цвет, который будет использоваться для комментариев. |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int-) | Позволяет указать цвет, который будет использоваться для удаленного контента.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int-) |  Позволяет указать эффект, который будет применяться к удаленному содержимому.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int-) |  Позволяет указать цвет, который будет использоваться для вставленного содержимого.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int-) |  Позволяет указать эффект, который будет применяться к вставленному содержимому.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int-) | Позволяет указать единицы измерения для комментариев к ревизии. |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int-) |  Позволяет указать цвет, который будет использоваться для областей, из которых было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int-) |  Позволяет указать эффект, который будет применяться к областям, из которых был перемещен контент.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int-) |  Позволяет указать цвет, который будет использоваться для областей, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int-) |  Позволяет указать эффект, который будет применяться к областям, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int-) |  Позволяет указать цвет, который будет использоваться для содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT). |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int-) |  Позволяет указать эффект для областей содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) не допускается и вызовет исключение java.lang.IllegalArgumentException. |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int-) | Позволяет указать цвет, который будет использоваться для боковых полос, обозначающих строки документа, содержащие исправленную информацию. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int-) | Устанавливает позицию рендеринга ревизионных стержней. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float-) | Задает ширину ревизионных полос в пунктах. |
| [setShowInBalloons(int value)](#setShowInBalloons-int-) | Позволяет указать, будут ли ревизии отображаться во всплывающих подсказках. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean-) | Позволяет указать, должен ли отображаться исходный текст вместо исправленного. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean-) | Позволяет указать, следует ли отображать полосы изменений рядом со строками, содержащими исправленное содержимое. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean-) | Позволяет указать, следует ли помечать текст ревизии специальной разметкой форматирования. |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCommentColor() {#getCommentColor--}
```
public int getCommentColor()
```


 Позволяет указать цвет, который будет использоваться для комментариев. Значение по умолчанию[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED) . Если установить для этого свойства значение[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) или же[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) значения, в результате для этого свойства будет установлен цвет по умолчанию.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getDeletedTextColor() {#getDeletedTextColor--}
```
public int getDeletedTextColor()
```


Позволяет указать цвет, который будет использоваться для удаленного контента.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getDeletedTextEffect() {#getDeletedTextEffect--}
```
public int getDeletedTextEffect()
```


 Позволяет указать эффект, который будет применяться к удаленному содержимому.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) . Значение по умолчанию[RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#STRIKE-THROUGH)

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы.
### getInsertedTextColor() {#getInsertedTextColor--}
```
public int getInsertedTextColor()
```


 Позволяет указать цвет, который будет использоваться для вставленного содержимого.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getInsertedTextEffect() {#getInsertedTextEffect--}
```
public int getInsertedTextEffect()
```


 Позволяет указать эффект, который будет применяться к вставленному содержимому.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) . Значение по умолчанию[RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect\#UNDERLINE) . значения[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) а также[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) не разрешены и вызовут исключение java.lang.IllegalArgumentException.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы.
### getMeasurementUnit() {#getMeasurementUnit--}
```
public int getMeasurementUnit()
```


Позволяет указать единицы измерения для комментариев к ревизии. Значение по умолчанию[MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits\#CENTIMETERS)

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MeasurementUnits](../../com.aspose.words/measurementunits) константы.
### getMovedFromTextColor() {#getMovedFromTextColor--}
```
public int getMovedFromTextColor()
```


 Позволяет указать цвет, который будет использоваться для областей, из которых было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getMovedFromTextEffect() {#getMovedFromTextEffect--}
```
public int getMovedFromTextEffect()
```


 Позволяет указать эффект, который будет применяться к областям, из которых был перемещен контент.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы.
### getMovedToTextColor() {#getMovedToTextColor--}
```
public int getMovedToTextColor()
```


 Позволяет указать цвет, который будет использоваться для областей, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getMovedToTextEffect() {#getMovedToTextEffect--}
```
public int getMovedToTextEffect()
```


 Позволяет указать эффект, который будет применяться к областям, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect\#DOUBLE-UNDERLINE) значения[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) а также[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) не разрешены и вызовут исключение java.lang.IllegalArgumentException.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы.
### getRevisedPropertiesColor() {#getRevisedPropertiesColor--}
```
public int getRevisedPropertiesColor()
```


 Позволяет указать цвет, который будет использоваться для содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect--}
```
public int getRevisedPropertiesEffect()
```


 Позволяет указать эффект для областей содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) не допускается и вызовет исключение java.lang.IllegalArgumentException.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы.
### getRevisionBarsColor() {#getRevisionBarsColor--}
```
public int getRevisionBarsColor()
```


 Позволяет указать цвет, который будет использоваться для боковых полос, обозначающих строки документа, содержащие исправленную информацию. Значение по умолчанию[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED) . Установка этого свойства в[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) или же[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) значения приведут к тому, что полосы ревизий будут скрыты от макета.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы.
### getRevisionBarsPosition() {#getRevisionBarsPosition--}
```
public int getRevisionBarsPosition()
```


 Получает позицию рендеринга исправлений. Значение по умолчанию[HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment\#OUTSIDE) . значения[HorizontalAlignment.CENTER](../../com.aspose.words/horizontalalignment\#CENTER) а также[HorizontalAlignment.INSIDE](../../com.aspose.words/horizontalalignment\#INSIDE) не разрешены и вызовут исключение java.lang.IllegalArgumentException.

**Возвращает:**
 int - Отрисовка положения штрихов ревизии. Возвращаемое значение является одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы.
### getRevisionBarsWidth() {#getRevisionBarsWidth--}
```
public float getRevisionBarsWidth()
```


Получает ширину ревизионных полос в пунктах.

**Возвращает:**
float - Ширина ревизионных баров, пункты.
### getShowInBalloons() {#getShowInBalloons--}
```
public int getShowInBalloons()
```


 Позволяет указать, будут ли ревизии отображаться во всплывающих подсказках. Значение по умолчанию[ShowInBalloons.NONE](../../com.aspose.words/showinballoons\#NONE) . Обратите внимание, что исправления не отображаются во всплывающих подсказках для[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ShowInBalloons](../../com.aspose.words/showinballoons) константы.
### getShowOriginalRevision() {#getShowOriginalRevision--}
```
public boolean getShowOriginalRevision()
```


Позволяет указать, должен ли отображаться исходный текст вместо исправленного. Значение по умолчанию — Ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowRevisionBars() {#getShowRevisionBars--}
```
public boolean getShowRevisionBars()
```


Позволяет указать, следует ли отображать полосы изменений рядом со строками, содержащими исправленное содержимое. Значение по умолчанию — Истина.

**Возвращает:**
boolean - соответствующее логическое значение.
### getShowRevisionMarks() {#getShowRevisionMarks--}
```
public boolean getShowRevisionMarks()
```


Позволяет указать, следует ли помечать текст ревизии специальной разметкой форматирования. Значение по умолчанию — Истина.

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




### setCommentColor(int value) {#setCommentColor-int-}
```
public void setCommentColor(int value)
```


 Позволяет указать цвет, который будет использоваться для комментариев. Значение по умолчанию[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED) . Если установить для этого свойства значение[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) или же[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) значения, в результате для этого свойства будет установлен цвет по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setDeletedTextColor(int value) {#setDeletedTextColor-int-}
```
public void setDeletedTextColor(int value)
```


Позволяет указать цвет, который будет использоваться для удаленного контента.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int-}
```
public void setDeletedTextEffect(int value)
```


 Позволяет указать эффект, который будет применяться к удаленному содержимому.[RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) . Значение по умолчанию[RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#STRIKE-THROUGH)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы. |

### setInsertedTextColor(int value) {#setInsertedTextColor-int-}
```
public void setInsertedTextColor(int value)
```


 Позволяет указать цвет, который будет использоваться для вставленного содержимого.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int-}
```
public void setInsertedTextEffect(int value)
```


 Позволяет указать эффект, который будет применяться к вставленному содержимому.[RevisionType.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) . Значение по умолчанию[RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect\#UNDERLINE) . значения[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) а также[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) не разрешены и вызовут исключение java.lang.IllegalArgumentException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы. |

### setMeasurementUnit(int value) {#setMeasurementUnit-int-}
```
public void setMeasurementUnit(int value)
```


Позволяет указать единицы измерения для комментариев к ревизии. Значение по умолчанию[MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits\#CENTIMETERS)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MeasurementUnits](../../com.aspose.words/measurementunits) константы. |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int-}
```
public void setMovedFromTextColor(int value)
```


 Позволяет указать цвет, который будет использоваться для областей, из которых было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int-}
```
public void setMovedFromTextEffect(int value)
```


 Позволяет указать эффект, который будет применяться к областям, из которых был перемещен контент.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы. |

### setMovedToTextColor(int value) {#setMovedToTextColor-int-}
```
public void setMovedToTextColor(int value)
```


 Позволяет указать цвет, который будет использоваться для областей, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int-}
```
public void setMovedToTextEffect(int value)
```


 Позволяет указать эффект, который будет применяться к областям, в которые было перемещено содержимое.[RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) . Значение по умолчанию[RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect\#DOUBLE-UNDERLINE) значения[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) а также[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH) не разрешены и вызовут исключение java.lang.IllegalArgumentException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы. |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int-}
```
public void setRevisedPropertiesColor(int value)
```


 Позволяет указать цвет, который будет использоваться для содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int-}
```
public void setRevisedPropertiesEffect(int value)
```


 Позволяет указать эффект для областей содержимого с изменением свойств форматирования.[RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) Значение по умолчанию[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN) не допускается и вызовет исключение java.lang.IllegalArgumentException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionTextEffect](../../com.aspose.words/revisiontexteffect) константы. |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int-}
```
public void setRevisionBarsColor(int value)
```


 Позволяет указать цвет, который будет использоваться для боковых полос, обозначающих строки документа, содержащие исправленную информацию. Значение по умолчанию[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED) . Установка этого свойства в[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR) или же[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT) значения приведут к тому, что полосы ревизий будут скрыты от макета.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[RevisionColor](../../com.aspose.words/revisioncolor) константы. |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int-}
```
public void setRevisionBarsPosition(int value)
```


Устанавливает позицию рендеринга ревизионных стержней. Значение по умолчанию[HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment\#OUTSIDE) . значения[HorizontalAlignment.CENTER](../../com.aspose.words/horizontalalignment\#CENTER) а также[HorizontalAlignment.INSIDE](../../com.aspose.words/horizontalalignment\#INSIDE) не разрешены и вызовут исключение java.lang.IllegalArgumentException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Отрисовка положения ревизионных стержней. Значение должно быть одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы. |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float-}
```
public void setRevisionBarsWidth(float value)
```


Задает ширину ревизионных полос в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Ширина ревизионных стержней, пунктов. |

### setShowInBalloons(int value) {#setShowInBalloons-int-}
```
public void setShowInBalloons(int value)
```


 Позволяет указать, будут ли ревизии отображаться во всплывающих подсказках. Значение по умолчанию[ShowInBalloons.NONE](../../com.aspose.words/showinballoons\#NONE) . Обратите внимание, что исправления не отображаются во всплывающих подсказках для[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ShowInBalloons](../../com.aspose.words/showinballoons) константы. |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean-}
```
public void setShowOriginalRevision(boolean value)
```


Позволяет указать, должен ли отображаться исходный текст вместо исправленного. Значение по умолчанию — Ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean-}
```
public void setShowRevisionBars(boolean value)
```


Позволяет указать, следует ли отображать полосы изменений рядом со строками, содержащими исправленное содержимое. Значение по умолчанию — Истина.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean-}
```
public void setShowRevisionMarks(boolean value)
```


Позволяет указать, следует ли помечать текст ревизии специальной разметкой форматирования. Значение по умолчанию — Истина.

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
