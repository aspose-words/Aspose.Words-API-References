---
title: ParagraphFormat
second_title: Справочник по API Aspose.Words для Java
description: Представляет все форматирование абзаца.
type: docs
weight: 446
url: /ru/java/com.aspose.words/paragraphformat/
---

**Наследование:**
java.lang.Object
```
public class ParagraphFormat
```

Представляет все форматирование абзаца.

 Чтобы узнать больше, посетите**Working with Paragraphs** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Восстанавливает форматирование абзаца по умолчанию. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha--) | Получает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце. |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit--) | Получает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями восточноазиатского текста в текущем абзаце. |
| [getAlignment()](#getAlignment--) | Получает выравнивание текста для абзаца. |
| [getBidi()](#getBidi--) | Получает, является ли это абзацем справа налево. |
| [getBorders()](#getBorders--) | Получает коллекцию границ абзаца. |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent--) | Получает значение (в символах) для первой строки или висячего отступа. |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent--) | Получает значение отступа слева (в символах) для указанных абзацев. |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent--) | Получает правильное значение отступа (в символах) для указанных абзацев. |
| [getClass()](#getClass--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDropCapPosition()](#getDropCapPosition--) | Получает позицию для текста буквицы. |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl--) | Получает флаг, указывающий, применяются ли восточноазиатские правила разрыва строк к текущему абзацу. |
| [getFirstLineIndent()](#getFirstLineIndent--) | Получает значение (в пунктах) для первой строки или висячего отступа. |
| [getHangingPunctuation()](#getHangingPunctuation--) | Получает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |
| [getKeepTogether()](#getKeepTogether--) | Истинно, если все строки в абзаце должны оставаться на одной странице. |
| [getKeepWithNext()](#getKeepWithNext--) | Истинно, если абзац должен оставаться на той же странице, что и абзац, следующий за ним. |
| [getLeftIndent()](#getLeftIndent--) | Получает значение (в пунктах), представляющее отступ слева для абзаца. |
| [getLineSpacing()](#getLineSpacing--) | Получает межстрочный интервал (в пунктах) для абзаца. |
| [getLineSpacingRule()](#getLineSpacingRule--) | Получает межстрочный интервал для абзаца. |
| [getLineUnitAfter()](#getLineUnitAfter--) | Получает количество интервалов (в линиях сетки) после абзацев. |
| [getLineUnitBefore()](#getLineUnitBefore--) | Получает величину интервала (в линиях сетки) перед абзацами. |
| [getLinesToDrop()](#getLinesToDrop--) | Получает количество строк текста абзаца, используемого для расчета высоты буквицы. |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle--) |  Когда правда,[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-) а также[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-) будет игнорироваться между абзацами одного стиля. |
| [getOutlineLevel()](#getOutlineLevel--) | Задает уровень структуры абзаца в документе. |
| [getPageBreakBefore()](#getPageBreakBefore--) | Истинно, если разрыв страницы принудительно ставится перед абзацем. |
| [getRightIndent()](#getRightIndent--) | Получает значение (в пунктах), представляющее правильный отступ для абзаца. |
| [getShading()](#getShading--) | Возвращает объект Shading, который ссылается на форматирование затенения абзаца. |
| [getSnapToGrid()](#getSnapToGrid--) | Указывает, должен ли текущий абзац использовать настройки линий сетки документа на странице при расположении содержимого в абзаце. |
| [getSpaceAfter()](#getSpaceAfter--) | Получает величину интервала (в пунктах) после абзаца. |
| [getSpaceAfterAuto()](#getSpaceAfterAuto--) | Истинно, если интервал после абзаца устанавливается автоматически. |
| [getSpaceBefore()](#getSpaceBefore--) | Получает величину интервала (в пунктах) перед абзацем. |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto--) | Истинно, если интервал перед абзацем устанавливается автоматически. |
| [getStyle()](#getStyle--) | Получает стиль абзаца, применяемый к этому форматированию. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Получает независимый от языкового стандарта идентификатор стиля абзаца, примененного к этому форматированию. |
| [getStyleName()](#getStyleName--) | Получает имя стиля абзаца, примененного к этому форматированию. |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens--) | Указывает, должен ли текущий абзац быть освобожден от любых переносов, которые применяются в настройках документа. |
| [getSuppressLineNumbers()](#getSuppressLineNumbers--) | Указывает, следует ли исключить строки текущего абзаца из нумерации строк, применяемой в родительском разделе. |
| [getTabStops()](#getTabStops--) | Получает коллекцию пользовательских позиций табуляции, определенных для этого объекта. |
| [getWidowControl()](#getWidowControl--) | Истинно, если первая и последняя строки в абзаце должны оставаться на той же странице, что и остальная часть абзаца. |
| [getWordWrap()](#getWordWrap--) |  Если это свойство**false**, Латинский текст в середине слова может переноситься на текущий абзац. |
| [hashCode()](#hashCode--) |  |
| [isHeading()](#isHeading--) | Значение true, если стиль абзаца является одним из встроенных стилей заголовков. |
| [isListItem()](#isListItem--) | Истинно, если абзац является элементом маркированного или нумерованного списка. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean-) | Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце. |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean-) | Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями восточноазиатского текста в текущем абзаце. |
| [setAlignment(int value)](#setAlignment-int-) | Устанавливает выравнивание текста для абзаца. |
| [setBidi(boolean value)](#setBidi-boolean-) | Устанавливает, является ли это абзацем справа налево. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double-) | Устанавливает значение (в символах) для первой строки или висячего отступа. |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double-) | Задает значение отступа слева (в символах) для указанных абзацев. |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double-) | Задает правильное значение отступа (в символах) для указанных абзацев. |
| [setDropCapPosition(int value)](#setDropCapPosition-int-) | Устанавливает позицию для текста буквицы. |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean-) | Устанавливает флаг, указывающий, применяются ли восточноазиатские правила разрыва строк к текущему абзацу. |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double-) | Устанавливает значение (в пунктах) для первой строки или висячего отступа. |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean-) | Устанавливает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean-) | Истинно, если все строки в абзаце должны оставаться на одной странице. |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean-) | Истинно, если абзац должен оставаться на той же странице, что и абзац, следующий за ним. |
| [setLeftIndent(double value)](#setLeftIndent-double-) | Задает значение (в пунктах), представляющее отступ слева для абзаца. |
| [setLineSpacing(double value)](#setLineSpacing-double-) | Устанавливает междустрочный интервал (в пунктах) для абзаца. |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int-) | Устанавливает межстрочный интервал для абзаца. |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double-) | Устанавливает величину интервала (в линиях сетки) после абзацев. |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double-) | Устанавливает величину интервала (в линиях сетки) перед абзацами. |
| [setLinesToDrop(int value)](#setLinesToDrop-int-) | Задает количество строк текста абзаца, используемого для расчета высоты буквицы. |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean-) |  Когда правда,[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-) а также[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-) будет игнорироваться между абзацами одного стиля. |
| [setOutlineLevel(int value)](#setOutlineLevel-int-) | Задает уровень структуры абзаца в документе. |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean-) | Истинно, если разрыв страницы принудительно ставится перед абзацем. |
| [setRightIndent(double value)](#setRightIndent-double-) | Задает значение (в пунктах), представляющее правый отступ для абзаца. |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean-) | Указывает, должен ли текущий абзац использовать настройки линий сетки документа на странице при расположении содержимого в абзаце. |
| [setSpaceAfter(double value)](#setSpaceAfter-double-) | Устанавливает величину интервала (в пунктах) после абзаца. |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean-) | Истинно, если интервал после абзаца устанавливается автоматически. |
| [setSpaceBefore(double value)](#setSpaceBefore-double-) | Устанавливает величину интервала (в пунктах) перед абзацем. |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean-) | Истинно, если интервал перед абзацем устанавливается автоматически. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Задает стиль абзаца, применяемый к этому форматированию. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | Задает независимый от локали идентификатор стиля абзаца, применяемого к этому форматированию. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Задает имя стиля абзаца, применяемого к этому форматированию. |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean-) | Указывает, должен ли текущий абзац быть освобожден от любых переносов, которые применяются в настройках документа. |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean-) | Указывает, следует ли исключить строки текущего абзаца из нумерации строк, применяемой в родительском разделе. |
| [setWidowControl(boolean value)](#setWidowControl-boolean-) | Истинно, если первая и последняя строки в абзаце должны оставаться на той же странице, что и остальная часть абзаца. |
| [setWordWrap(boolean value)](#setWordWrap-boolean-) |  Если это свойство**false**, Латинский текст в середине слова может переноситься на текущий абзац. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Восстанавливает форматирование абзаца по умолчанию. Форматирование абзаца по умолчанию — обычный стиль, выравнивание по левому краю, без отступов, без интервалов, без границ и без заливки.

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
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha--}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


Получает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце.

**Возвращает:**
boolean — флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце.
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit--}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


Получает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями восточноазиатского текста в текущем абзаце.

**Возвращает:**
boolean — флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями восточноазиатского текста в текущем абзаце.
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Получает выравнивание текста для абзаца.

**Возвращает:**
int — выравнивание текста для абзаца. Возвращаемое значение является одним из[ParagraphAlignment](../../com.aspose.words/paragraphalignment) константы.
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Получает, является ли это абзацем справа налево.

Если задано значение true, прогоны и другие встроенные объекты в этом абзаце располагаются справа налево.

**Возвращает:**
boolean - Является ли это абзацем справа налево.
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ абзаца.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Коллекция границ абзаца.
### getCharacterUnitFirstLineIndent() {#getCharacterUnitFirstLineIndent--}
```
public double getCharacterUnitFirstLineIndent()
```


Получает значение (в символах) для первой строки или висячего отступа.

Используйте положительные значения, чтобы установить отступ первой строки, и отрицательные значения, чтобы установить выступ.

**Возвращает:**
double — значение (в символах) для первой строки или выступа.
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent--}
```
public double getCharacterUnitLeftIndent()
```


Получает значение отступа слева (в символах) для указанных абзацев.

**Возвращает:**
double — значение отступа слева (в символах) для указанных абзацев.
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent--}
```
public double getCharacterUnitRightIndent()
```


Получает правильное значение отступа (в символах) для указанных абзацев.

**Возвращает:**
double - Значение правого отступа (в символах) для указанных абзацев.
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
### getDropCapPosition() {#getDropCapPosition--}
```
public int getDropCapPosition()
```


Получает позицию для текста буквицы.

**Возвращает:**
 int - Позиция для текста буквицы. Возвращаемое значение является одним из[DropCapPosition](../../com.aspose.words/dropcapposition) константы.
### getFarEastLineBreakControl() {#getFarEastLineBreakControl--}
```
public boolean getFarEastLineBreakControl()
```


Получает флаг, указывающий, применяются ли восточноазиатские правила разрыва строк к текущему абзацу.

**Возвращает:**
boolean — Флаг, указывающий, применяются ли к текущему абзацу восточноазиатские правила разрыва строк.
### getFirstLineIndent() {#getFirstLineIndent--}
```
public double getFirstLineIndent()
```


Получает значение (в пунктах) для первой строки или висячего отступа.

Используйте положительные значения, чтобы установить отступ первой строки, и отрицательные значения, чтобы установить выступ.

**Возвращает:**
double - значение (в пунктах) для первой строки или выступа.
### getHangingPunctuation() {#getHangingPunctuation--}
```
public boolean getHangingPunctuation()
```


Получает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

**Возвращает:**
boolean - Флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.
### getKeepTogether() {#getKeepTogether--}
```
public boolean getKeepTogether()
```


Истинно, если все строки в абзаце должны оставаться на одной странице.

**Возвращает:**
boolean - соответствующее логическое значение.
### getKeepWithNext() {#getKeepWithNext--}
```
public boolean getKeepWithNext()
```


Истинно, если абзац должен оставаться на той же странице, что и абзац, следующий за ним.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


Получает значение (в пунктах), представляющее отступ слева для абзаца.

**Возвращает:**
double — значение (в пунктах), представляющее левый отступ для абзаца.
### getLineSpacing() {#getLineSpacing--}
```
public double getLineSpacing()
```


Получает межстрочный интервал (в пунктах) для абзаца.

Если для свойства LineSpacingRule установлено значение AtLeast, межстрочный интервал может быть больше или равен, но не меньше указанного значения LineSpacing.

Когда для свойства LineSpacingRule задано значение Exactly, междустрочный интервал никогда не изменяется по сравнению с указанным значением LineSpacing, даже если в абзаце используется более крупный шрифт.

**Возвращает:**
double - межстрочный интервал (в пунктах) для абзаца.
### getLineSpacingRule() {#getLineSpacingRule--}
```
public int getLineSpacingRule()
```


Получает межстрочный интервал для абзаца.

**Возвращает:**
 int - межстрочный интервал для абзаца. Возвращаемое значение является одним из[LineSpacingRule](../../com.aspose.words/linespacingrule) константы.
### getLineUnitAfter() {#getLineUnitAfter--}
```
public double getLineUnitAfter()
```


Получает количество интервалов (в линиях сетки) после абзацев.

**Возвращает:**
double - количество интервалов (в линиях сетки) после абзацев.
### getLineUnitBefore() {#getLineUnitBefore--}
```
public double getLineUnitBefore()
```


Получает величину интервала (в линиях сетки) перед абзацами.

**Возвращает:**
double - количество интервалов (в линиях сетки) перед абзацами.
### getLinesToDrop() {#getLinesToDrop--}
```
public int getLinesToDrop()
```


Получает количество строк текста абзаца, используемого для расчета высоты буквицы.

**Возвращает:**
int — количество строк текста абзаца, используемое для расчета высоты буквицы.
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle--}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


 Когда правда,[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-) а также[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-) будет игнорироваться между абзацами одного стиля.

Этот параметр действует только при применении к стилю абзаца. Если он применяется к абзацу напрямую, он не имеет никакого эффекта.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOutlineLevel() {#getOutlineLevel--}
```
public int getOutlineLevel()
```


Задает уровень структуры абзаца в документе.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[OutlineLevel](../../com.aspose.words/outlinelevel) константы.
### getPageBreakBefore() {#getPageBreakBefore--}
```
public boolean getPageBreakBefore()
```


Истинно, если разрыв страницы принудительно ставится перед абзацем.

**Возвращает:**
boolean - соответствующее логическое значение.
### getRightIndent() {#getRightIndent--}
```
public double getRightIndent()
```


Получает значение (в пунктах), представляющее правильный отступ для абзаца.

**Возвращает:**
double — значение (в пунктах), представляющее правый отступ для абзаца.
### getShading() {#getShading--}
```
public Shading getShading()
```


Возвращает объект Shading, который ссылается на форматирование затенения абзаца.

**Возвращает:**
[Shading](../../com.aspose.words/shading) Объект Shading, который ссылается на форматирование затенения абзаца.
### getSnapToGrid() {#getSnapToGrid--}
```
public boolean getSnapToGrid()
```


Указывает, должен ли текущий абзац использовать настройки линий сетки документа на странице при расположении содержимого в абзаце.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpaceAfter() {#getSpaceAfter--}
```
public double getSpaceAfter()
```


Получает величину интервала (в пунктах) после абзаца.

 Не действует, когда[getSpaceAfterAuto()](../../com.aspose.words/paragraphformat\#getSpaceAfterAuto--) / [setSpaceAfterAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceAfterAuto-boolean-) правда.

 Допустимые значения\в\Диапазон от 0 до 1584 включительно.

**Возвращает:**
double - количество интервалов (в пунктах) после абзаца.
### getSpaceAfterAuto() {#getSpaceAfterAuto--}
```
public boolean getSpaceAfterAuto()
```


Истинно, если интервал после абзаца устанавливается автоматически.

 Если установлено значение true, переопределяет эффект[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-).

Если для параметра «Отступ перед абзацем» и «Отступ после» задано значение «Авто», Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Обычно интервал добавляется после всех абзацев.
 *  В маркированном или нумерованном списке пробел добавляется только после последнего элемента в списке. Интервал не добавляется между элементами списка.
 *  Во вложенных маркированных или нумерованных списках интервал не добавляется.
 *  Пробел обычно добавляется после таблицы.
 *  Пробел не добавляется после таблицы, если это последний блок в ячейке таблицы.
 *  Интервал не добавляется после последнего абзаца в ячейке таблицы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSpaceBefore() {#getSpaceBefore--}
```
public double getSpaceBefore()
```


Получает величину интервала (в пунктах) перед абзацем.

 Не действует, когда[getSpaceBeforeAuto()](../../com.aspose.words/paragraphformat\#getSpaceBeforeAuto--) / [setSpaceBeforeAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceBeforeAuto-boolean-) правда.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

**Возвращает:**
double - количество интервалов (в пунктах) перед абзацем.
### getSpaceBeforeAuto() {#getSpaceBeforeAuto--}
```
public boolean getSpaceBeforeAuto()
```


Истинно, если интервал перед абзацем устанавливается автоматически.

 Если установлено значение true, переопределяет эффект[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-).

Если для параметра «Отступ перед абзацем» и «Отступ после» задано значение «Авто», Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Обычно интервал добавляется после всех абзацев.
 *  В маркированном или нумерованном списке пробел добавляется только после последнего элемента в списке. Интервал не добавляется между элементами списка.
 *  Во вложенных маркированных или нумерованных списках интервал не добавляется.
 *  Пробел обычно добавляется после таблицы.
 *  Пробел не добавляется после таблицы, если это последний блок в ячейке таблицы.
 *  Интервал не добавляется после последнего абзаца в ячейке таблицы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


Получает стиль абзаца, применяемый к этому форматированию.

**Возвращает:**
[Style](../../com.aspose.words/style) Стиль абзаца, примененный к этому форматированию.
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Получает независимый от языкового стандарта идентификатор стиля абзаца, примененного к этому форматированию.

**Возвращает:**
 int — независимый от локали идентификатор стиля абзаца, примененный к этому форматированию. Возвращаемое значение является одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы.
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Получает имя стиля абзаца, примененного к этому форматированию.

**Возвращает:**
java.lang.String — имя стиля абзаца, примененного к этому форматированию.
### getSuppressAutoHyphens() {#getSuppressAutoHyphens--}
```
public boolean getSuppressAutoHyphens()
```


Указывает, должен ли текущий абзац быть освобожден от любых переносов, которые применяются в настройках документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSuppressLineNumbers() {#getSuppressLineNumbers--}
```
public boolean getSuppressLineNumbers()
```


Указывает, следует ли исключить строки текущего абзаца из нумерации строк, применяемой в родительском разделе.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTabStops() {#getTabStops--}
```
public TabStopCollection getTabStops()
```


Получает коллекцию пользовательских позиций табуляции, определенных для этого объекта.

**Возвращает:**
[TabStopCollection](../../com.aspose.words/tabstopcollection) - Коллекция пользовательских табуляторов, определенных для этого объекта.
### getWidowControl() {#getWidowControl--}
```
public boolean getWidowControl()
```


Истинно, если первая и последняя строки в абзаце должны оставаться на той же странице, что и остальная часть абзаца.

**Возвращает:**
boolean - соответствующее логическое значение.
### getWordWrap() {#getWordWrap--}
```
public boolean getWordWrap()
```


 Если это свойство**false**, Латинский текст в середине слова может переноситься на текущий абзац. В противном случае латинский текст переносится целыми словами.

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isHeading() {#isHeading--}
```
public boolean isHeading()
```


Значение true, если стиль абзаца является одним из встроенных стилей заголовков.

**Возвращает:**
boolean - соответствующее логическое значение.
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


Истинно, если абзац является элементом маркированного или нумерованного списка.

**Возвращает:**
boolean - соответствующее логическое значение.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean-}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце. |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean-}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


Устанавливает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями восточноазиатского текста в текущем абзаце.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями чисел и областями восточноазиатского текста в текущем абзаце. |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Устанавливает выравнивание текста для абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Выравнивание текста для абзаца. Значение должно быть одним из[ParagraphAlignment](../../com.aspose.words/paragraphalignment) константы. |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Устанавливает, является ли это абзацем справа налево.

Если задано значение true, прогоны и другие встроенные объекты в этом абзаце располагаются справа налево.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Является ли это абзацем справа налево. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double-}
```
public void setCharacterUnitFirstLineIndent(double value)
```


Устанавливает значение (в символах) для первой строки или висячего отступа.

Используйте положительные значения, чтобы установить отступ первой строки, и отрицательные значения, чтобы установить выступ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение (в символах) для первой строки или висячего отступа. |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double-}
```
public void setCharacterUnitLeftIndent(double value)
```


Задает значение отступа слева (в символах) для указанных абзацев.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение отступа слева (в символах) для указанных абзацев. |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double-}
```
public void setCharacterUnitRightIndent(double value)
```


Задает правильное значение отступа (в символах) для указанных абзацев.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение правого отступа (в символах) для указанных абзацев. |

### setDropCapPosition(int value) {#setDropCapPosition-int-}
```
public void setDropCapPosition(int value)
```


Устанавливает позицию для текста буквицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Позиция для текста буквицы. Значение должно быть одним из[DropCapPosition](../../com.aspose.words/dropcapposition) константы. |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean-}
```
public void setFarEastLineBreakControl(boolean value)
```


Устанавливает флаг, указывающий, применяются ли восточноазиатские правила разрыва строк к текущему абзацу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, применяются ли восточноазиатские правила разрыва строк к текущему абзацу. |

### setFirstLineIndent(double value) {#setFirstLineIndent-double-}
```
public void setFirstLineIndent(double value)
```


Устанавливает значение (в пунктах) для первой строки или висячего отступа.

Используйте положительные значения, чтобы установить отступ первой строки, и отрицательные значения, чтобы установить выступ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение (в пунктах) для первой строки или висячего отступа. |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean-}
```
public void setHangingPunctuation(boolean value)
```


Устанавливает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, включена ли висячая пунктуация для текущего абзаца. |

### setKeepTogether(boolean value) {#setKeepTogether-boolean-}
```
public void setKeepTogether(boolean value)
```


Истинно, если все строки в абзаце должны оставаться на одной странице.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean-}
```
public void setKeepWithNext(boolean value)
```


Истинно, если абзац должен оставаться на той же странице, что и абзац, следующий за ним.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


Задает значение (в пунктах), представляющее отступ слева для абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение (в пунктах), представляющее отступ слева для абзаца. |

### setLineSpacing(double value) {#setLineSpacing-double-}
```
public void setLineSpacing(double value)
```


Устанавливает междустрочный интервал (в пунктах) для абзаца.

Если для свойства LineSpacingRule установлено значение AtLeast, межстрочный интервал может быть больше или равен, но не меньше указанного значения LineSpacing.

Когда для свойства LineSpacingRule задано значение Exactly, междустрочный интервал никогда не изменяется по сравнению с указанным значением LineSpacing, даже если в абзаце используется более крупный шрифт.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Межстрочный интервал (в пунктах) для абзаца. |

### setLineSpacingRule(int value) {#setLineSpacingRule-int-}
```
public void setLineSpacingRule(int value)
```


Устанавливает межстрочный интервал для абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Межстрочный интервал для абзаца. Значение должно быть одним из[LineSpacingRule](../../com.aspose.words/linespacingrule) константы. |

### setLineUnitAfter(double value) {#setLineUnitAfter-double-}
```
public void setLineUnitAfter(double value)
```


Устанавливает величину интервала (в линиях сетки) после абзацев.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество интервалов (в линиях сетки) после абзацев. |

### setLineUnitBefore(double value) {#setLineUnitBefore-double-}
```
public void setLineUnitBefore(double value)
```


Устанавливает величину интервала (в линиях сетки) перед абзацами.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Размер интервала (в линиях сетки) перед абзацами. |

### setLinesToDrop(int value) {#setLinesToDrop-int-}
```
public void setLinesToDrop(int value)
```


Задает количество строк текста абзаца, используемого для расчета высоты буквицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество строк текста абзаца, используемое для расчета высоты буквицы. |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean-}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


 Когда правда,[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-) а также[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-) будет игнорироваться между абзацами одного стиля.

Этот параметр действует только при применении к стилю абзаца. Если он применяется к абзацу напрямую, он не имеет никакого эффекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOutlineLevel(int value) {#setOutlineLevel-int-}
```
public void setOutlineLevel(int value)
```


Задает уровень структуры абзаца в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[OutlineLevel](../../com.aspose.words/outlinelevel) константы. |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean-}
```
public void setPageBreakBefore(boolean value)
```


Истинно, если разрыв страницы принудительно ставится перед абзацем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setRightIndent(double value) {#setRightIndent-double-}
```
public void setRightIndent(double value)
```


Задает значение (в пунктах), представляющее правый отступ для абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение (в пунктах), представляющее отступ справа для абзаца. |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean-}
```
public void setSnapToGrid(boolean value)
```


Указывает, должен ли текущий абзац использовать настройки линий сетки документа на странице при расположении содержимого в абзаце.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpaceAfter(double value) {#setSpaceAfter-double-}
```
public void setSpaceAfter(double value)
```


Устанавливает величину интервала (в пунктах) после абзаца.

 Не действует, когда[getSpaceAfterAuto()](../../com.aspose.words/paragraphformat\#getSpaceAfterAuto--) / [setSpaceAfterAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceAfterAuto-boolean-) правда.

 Допустимые значения\в\Диапазон от 0 до 1584 включительно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) после абзаца. |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean-}
```
public void setSpaceAfterAuto(boolean value)
```


Истинно, если интервал после абзаца устанавливается автоматически.

 Если установлено значение true, переопределяет эффект[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-).

Если для параметра «Отступ перед абзацем» и «Отступ после» задано значение «Авто», Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Обычно интервал добавляется после всех абзацев.
 *  В маркированном или нумерованном списке пробел добавляется только после последнего элемента в списке. Интервал не добавляется между элементами списка.
 *  Во вложенных маркированных или нумерованных списках интервал не добавляется.
 *  Пробел обычно добавляется после таблицы.
 *  Пробел не добавляется после таблицы, если это последний блок в ячейке таблицы.
 *  Интервал не добавляется после последнего абзаца в ячейке таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSpaceBefore(double value) {#setSpaceBefore-double-}
```
public void setSpaceBefore(double value)
```


Устанавливает величину интервала (в пунктах) перед абзацем.

 Не действует, когда[getSpaceBeforeAuto()](../../com.aspose.words/paragraphformat\#getSpaceBeforeAuto--) / [setSpaceBeforeAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceBeforeAuto-boolean-) правда.

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) перед абзацем. |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean-}
```
public void setSpaceBeforeAuto(boolean value)
```


Истинно, если интервал перед абзацем устанавливается автоматически.

 Если установлено значение true, переопределяет эффект[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-).

Если для параметра «Отступ перед абзацем» и «Отступ после» задано значение «Авто», Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

 *  Обычно интервал добавляется после всех абзацев.
 *  В маркированном или нумерованном списке пробел добавляется только после последнего элемента в списке. Интервал не добавляется между элементами списка.
 *  Во вложенных маркированных или нумерованных списках интервал не добавляется.
 *  Пробел обычно добавляется после таблицы.
 *  Пробел не добавляется после таблицы, если это последний блок в ячейке таблицы.
 *  Интервал не добавляется после последнего абзаца в ячейке таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


Задает стиль абзаца, применяемый к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | Стиль абзаца, примененный к этому форматированию. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


Задает независимый от локали идентификатор стиля абзаца, применяемого к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Независимый от локали идентификатор стиля абзаца, примененный к этому форматированию. Значение должно быть одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы. |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Задает имя стиля абзаца, применяемого к этому форматированию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя стиля абзаца, примененного к этому форматированию. |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean-}
```
public void setSuppressAutoHyphens(boolean value)
```


Указывает, должен ли текущий абзац быть освобожден от любых переносов, которые применяются в настройках документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean-}
```
public void setSuppressLineNumbers(boolean value)
```


Указывает, следует ли исключить строки текущего абзаца из нумерации строк, применяемой в родительском разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setWidowControl(boolean value) {#setWidowControl-boolean-}
```
public void setWidowControl(boolean value)
```


Истинно, если первая и последняя строки в абзаце должны оставаться на той же странице, что и остальная часть абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setWordWrap(boolean value) {#setWordWrap-boolean-}
```
public void setWordWrap(boolean value)
```


 Если это свойство**false**, Латинский текст в середине слова может переноситься на текущий абзац. В противном случае латинский текст переносится целыми словами.

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
