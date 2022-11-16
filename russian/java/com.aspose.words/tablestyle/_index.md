---
title: TableStyle
second_title: Справочник по API Aspose.Words для Java
description: Представляет стиль таблицы.
type: docs
weight: 552
url: /ru/java/com.aspose.words/tablestyle/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Style](../../com.aspose.words/style)
```
public class TableStyle extends Style
```

Представляет стиль таблицы.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs--) |  |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRowAttrs()](#clearRowAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Style style)](#equals-com.aspose.words.Style-) | Сравнивается с указанным стилем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int-) |  |
| [getAliases()](#getAliases--) | Получает все псевдонимы этого стиля. |
| [getAlignment()](#getAlignment--) | Задает выравнивание для стиля таблицы. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages--) | Получает флаг, указывающий, разрешено ли разбиение текста в строке таблицы на разрыв страницы. |
| [getBaseStyleName()](#getBaseStyleName--) | Получает/задает имя стиля, на котором основан этот стиль. |
| [getBidi()](#getBidi--) | Получает, является ли это стилем для таблицы с письмом справа налево. |
| [getBorders()](#getBorders--) | Получает коллекцию границ ячеек по умолчанию для стиля. |
| [getBottomPadding()](#getBottomPadding--) | Получает количество места (в пунктах) для добавления под содержимым ячеек таблицы. |
| [getBuiltIn()](#getBuiltIn--) | Истинно, если этот стиль является одним из встроенных стилей в MS Word. |
| [getCellSpacing()](#getCellSpacing--) | Получает расстояние (в пунктах) между ячейками. |
| [getClass()](#getClass--) |  |
| [getColumnStripe()](#getColumnStripe--) | Получает количество столбцов для включения в полосу, когда стиль указывает полосу нечетных/четных столбцов. |
| [getConditionalStyles()](#getConditionalStyles--) | Коллекция условных стилей, которые могут быть определены для этого стиля таблицы. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int-) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ владельца. |
| [getFont()](#getFont--) | Получает форматирование символов стиля. |
| [getLeftIndent()](#getLeftIndent--) | Получает значение, представляющее левый отступ таблицы. |
| [getLeftPadding()](#getLeftPadding--) | Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячеек таблицы. |
| [getLinkedStyleName()](#getLinkedStyleName--) | Получает имя стиля, связанного с этим. |
| [getList()](#getList--) | Получает список, определяющий форматирование этого стиля списка. |
| [getListFormat()](#getListFormat--) | Предоставляет доступ к свойствам форматирования списка стиля абзаца. |
| [getName()](#getName--) | Получает имя стиля. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName--) | Получает/задает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного с использованием указанного стиля. |
| [getParagraphFormat()](#getParagraphFormat--) | Получает форматирование абзаца стиля. |
| [getRightPadding()](#getRightPadding--) | Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы. |
| [getRowStripe()](#getRowStripe--) | Получает количество строк для включения в полосу, когда стиль указывает полосу нечетных/четных строк. |
| [getShading()](#getShading--) | Получает[Shading](../../com.aspose.words/shading) объект, который относится к форматированию затенения для ячеек таблицы. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Получает независимый от языкового стандарта идентификатор стиля для встроенного стиля. |
| [getStyles()](#getStyles--) | Получает коллекцию стилей, к которым принадлежит этот стиль. |
| [getTopPadding()](#getTopPadding--) | Получает количество места (в пунктах) для добавления над содержимым ячеек таблицы. |
| [getType()](#getType--) | Получает тип стиля (абзац или символ). |
| [getVerticalAlignment()](#getVerticalAlignment--) | Указывает вертикальное выравнивание ячеек. |
| [hashCode()](#hashCode--) |  |
| [isHeading()](#isHeading--) | True, если стиль является одним из встроенных стилей заголовков. |
| [isQuickStyle()](#isQuickStyle--) | Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean-) | Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет указанный стиль из документа. |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs--) |  |
| [setAlignment(int value)](#setAlignment-int-) | Задает выравнивание для стиля таблицы. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean-) | Устанавливает флаг, указывающий, разрешено ли разбивать текст в строке таблицы через разрыв страницы. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String-) | Получает/задает имя стиля, на котором основан этот стиль. |
| [setBidi(boolean value)](#setBidi-boolean-) | Устанавливает, является ли это стилем для таблицы с письмом справа налево. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Устанавливает количество места (в пунктах) для добавления под содержимым ячеек таблицы. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object-) |  |
| [setCellSpacing(double value)](#setCellSpacing-double-) | Устанавливает расстояние (в пунктах) между ячейками. |
| [setColumnStripe(int value)](#setColumnStripe-int-) | Устанавливает количество столбцов для включения в полосу, когда стиль определяет полосу нечетных/четных столбцов. |
| [setLeftIndent(double value)](#setLeftIndent-double-) | Задает значение, представляющее левый отступ таблицы. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Задает количество места (в пунктах), добавляемого слева от содержимого ячеек таблицы. |
| [setName(String value)](#setName-java.lang.String-) | Устанавливает имя стиля. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String-) | Получает/задает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного с использованием указанного стиля. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRightPadding(double value)](#setRightPadding-double-) | Задает количество места (в пунктах), добавляемого справа от содержимого ячеек таблицы. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object-) |  |
| [setRowStripe(int value)](#setRowStripe-int-) | Устанавливает количество строк для включения в полосу, когда стиль определяет полосу нечетных/четных строк. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setTopPadding(double value)](#setTopPadding-double-) | Устанавливает количество места (в пунктах) для добавления над содержимым ячеек таблицы. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Указывает вертикальное выравнивание ячеек. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearCellAttrs() {#clearCellAttrs--}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs--}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style-}
```
public boolean equals(Style style)
```


Сравнивается с указанным стилем. Стили Istds сравниваются только для встроенных стилей. Стили по умолчанию не включены в сравнение. Базовый стиль, связанный стиль и стиль следующего абзаца сравниваются рекурсивно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) |  |

**Возвращает:**
логический
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
### fetchCellAttr(int key) {#fetchCellAttr-int-}
```
public Object fetchCellAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
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
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int-}
```
public Object fetchInheritedCellAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int-}
```
public Object fetchInheritedRowAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
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
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchRowAttr(int key) {#fetchRowAttr-int-}
```
public Object fetchRowAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getAliases() {#getAliases--}
```
public String[] getAliases()
```


Получает все псевдонимы этого стиля. Если стиль не имеет псевдонимов, то возвращается пустой массив строк.

**Возвращает:**
java.lang.String[] - Все псевдонимы этого стиля.
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


 Задает выравнивание для стиля таблицы. Значение по умолчанию[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[TableAlignment](../../com.aspose.words/tablealignment) константы.
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages--}
```
public boolean getAllowBreakAcrossPages()
```


 Получает флаг, указывающий, разрешено ли разбиение текста в строке таблицы на разрыв страницы. Значение по умолчанию**true**.

**Возвращает:**
boolean — Флаг, указывающий, разрешено ли разбивать текст в строке таблицы через разрыв страницы.
### getBaseStyleName() {#getBaseStyleName--}
```
public String getBaseStyleName()
```


Получает/задает имя стиля, на котором основан этот стиль. Это будет пустая строка, если стиль не основан ни на каком другом стиле и может быть установлен в пустую строку.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Получает, является ли это стилем для таблицы с письмом справа налево.

 Когда**true**, ячейки в строках располагаются справа налево.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - Является ли это стилем для таблицы с письмом справа налево.
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ ячеек по умолчанию для стиля.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Коллекция границ ячеек по умолчанию для стиля.
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Получает количество места (в пунктах) для добавления под содержимым ячеек таблицы.

**Возвращает:**
double - количество места (в пунктах), которое нужно добавить под содержимым ячеек таблицы.
### getBuiltIn() {#getBuiltIn--}
```
public boolean getBuiltIn()
```


Истинно, если этот стиль является одним из встроенных стилей в MS Word.

**Возвращает:**
boolean - соответствующее логическое значение.
### getCellSpacing() {#getCellSpacing--}
```
public double getCellSpacing()
```


Получает расстояние (в пунктах) между ячейками.

**Возвращает:**
double - количество пробелов (в пунктах) между ячейками.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColumnStripe() {#getColumnStripe--}
```
public int getColumnStripe()
```


Получает количество столбцов для включения в полосу, когда стиль указывает полосу нечетных/четных столбцов.

**Возвращает:**
int — количество столбцов для включения в полосу, когда стиль определяет полосу нечетных/четных столбцов.
### getConditionalStyles() {#getConditionalStyles--}
```
public ConditionalStyleCollection getConditionalStyles()
```


Коллекция условных стилей, которые могут быть определены для этого стиля таблицы.

**Возвращает:**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection) - соответствующий[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection) ценность.
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
### getDirectCellAttr(int key) {#getDirectCellAttr-int-}
```
public Object getDirectCellAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Возвращает:**
java.lang.Объект
### getDirectRowAttr(int key) {#getDirectRowAttr-int-}
```
public Object getDirectRowAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ владельца.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ собственника.
### getFont() {#getFont--}
```
public Font getFont()
```


Получает форматирование символов стиля.

Для стилей списка это свойство возвращает значение null.

**Возвращает:**
[Font](../../com.aspose.words/font) - Форматирование символов стиля.
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


Получает значение, представляющее левый отступ таблицы.

**Возвращает:**
double — значение, представляющее левый отступ таблицы.
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Получает количество места (в пунктах), которое нужно добавить слева от содержимого ячеек таблицы.

**Возвращает:**
double - Количество места (в пунктах) для добавления слева от содержимого ячеек таблицы.
### getLinkedStyleName() {#getLinkedStyleName--}
```
public String getLinkedStyleName()
```


Получает имя стиля, связанного с этим. Возвращает пустую строку, если стили не связаны.

**Возвращает:**
java.lang.String — имя стиля, связанного с этим.
### getList() {#getList--}
```
public List getList()
```


Получает список, определяющий форматирование этого стиля списка.

Это свойство допустимо только для стилей списка. Для других типов стилей это свойство возвращает значение null.

**Возвращает:**
[List](../../com.aspose.words/list) - Список, определяющий форматирование этого стиля списка.
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


Предоставляет доступ к свойствам форматирования списка стиля абзаца.

Это свойство допустимо только для стилей абзаца. Для других типов стилей это свойство возвращает значение null.

**Возвращает:**
[ListFormat](../../com.aspose.words/listformat) - соответствующий[ListFormat](../../com.aspose.words/listformat) ценность.
### getName() {#getName--}
```
public String getName()
```


Получает имя стиля.

Не может быть пустой строкой.

Если в коллекции уже есть стиль с таким именем, то этот стиль переопределит его. Все затронутые узлы будут ссылаться на новый стиль.

**Возвращает:**
java.lang.String — имя стиля.
### getNextParagraphStyleName() {#getNextParagraphStyleName--}
```
public String getNextParagraphStyleName()
```


Получает/задает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного с использованием указанного стиля. Это свойство не используется Aspose.Words. Следующий стиль абзаца будет применяться автоматически только при редактировании документа в MS Word.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Получает форматирование абзаца стиля.

Для стилей символов и списков это свойство возвращает значение null.

**Возвращает:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - Стиль форматирования абзаца.
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Получает количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы.

**Возвращает:**
double - Количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы.
### getRowStripe() {#getRowStripe--}
```
public int getRowStripe()
```


Получает количество строк для включения в полосу, когда стиль указывает полосу нечетных/четных строк.

**Возвращает:**
int — количество строк для включения в полосу, когда стиль определяет полосу нечетных/четных строк.
### getShading() {#getShading--}
```
public Shading getShading()
```


Получает[Shading](../../com.aspose.words/shading) объект, который относится к форматированию затенения для ячеек таблицы.

**Возвращает:**
[Shading](../../com.aspose.words/shading) - А[Shading](../../com.aspose.words/shading) объект, который относится к форматированию затенения для ячеек таблицы.
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Получает независимый от языкового стандарта идентификатор стиля для встроенного стиля.

 Для пользовательских (настраиваемых) стилей это свойство возвращает[StyleIdentifier.USER](../../com.aspose.words/styleidentifier\#USER).

**Возвращает:**
int — независимый от локали идентификатор стиля для встроенного стиля. Возвращаемое значение является одним из[StyleIdentifier](../../com.aspose.words/styleidentifier) константы.
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


Получает коллекцию стилей, к которым принадлежит этот стиль.

**Возвращает:**
[StyleCollection](../../com.aspose.words/stylecollection) - Коллекция стилей, к которым принадлежит этот стиль.
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Получает количество места (в пунктах) для добавления над содержимым ячеек таблицы.

**Возвращает:**
double — количество места (в пунктах), которое нужно добавить над содержимым ячеек таблицы.
### getType() {#getType--}
```
public int getType()
```


Получает тип стиля (абзац или символ).

**Возвращает:**
 int - Тип стиля (абзац или символ). Возвращаемое значение является одним из[StyleType](../../com.aspose.words/styletype) константы.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


 Указывает вертикальное выравнивание ячеек. Значение по умолчанию[CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment\#TOP).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment) константы.
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


True, если стиль является одним из встроенных стилей заголовков.

**Возвращает:**
boolean - соответствующее логическое значение.
### isQuickStyle() {#isQuickStyle--}
```
public boolean isQuickStyle()
```


Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word.

**Возвращает:**
boolean - соответствующее логическое значение.
### isQuickStyle(boolean value) {#isQuickStyle-boolean-}
```
public void isQuickStyle(boolean value)
```


Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public void remove()
```


Удаляет указанный стиль из документа. Удаление стиля влияет на модель документа следующим образом:

 *  Все ссылки на стиль удаляются из соответствующих абзацев, прогонов и таблиц.
 *  Если базовый стиль удаляется, его форматирование перемещается в дочерние стили.
 *  Если стиль, подлежащий удалению, имеет связанный стиль, то удаляются оба стиля.

### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs--}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


 Задает выравнивание для стиля таблицы. Значение по умолчанию[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[TableAlignment](../../com.aspose.words/tablealignment) константы. |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean-}
```
public void setAllowBreakAcrossPages(boolean value)
```


 Устанавливает флаг, указывающий, разрешено ли разбивать текст в строке таблицы через разрыв страницы. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, разрешено ли разбивать текст в строке таблицы через разрыв страницы. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String-}
```
public void setBaseStyleName(String value)
```


Получает/задает имя стиля, на котором основан этот стиль. Это будет пустая строка, если стиль не основан ни на каком другом стиле и может быть установлен в пустую строку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Устанавливает, является ли это стилем для таблицы с письмом справа налево.

 Когда**true**, ячейки в строках располагаются справа налево.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Является ли это стилем для таблицы справа налево. |

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


Устанавливает количество места (в пунктах) для добавления под содержимым ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить под содержимым ячеек таблицы. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object-}
```
public void setCellAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double-}
```
public void setCellSpacing(double value)
```


Устанавливает расстояние (в пунктах) между ячейками.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Расстояние (в пунктах) между ячейками. |

### setColumnStripe(int value) {#setColumnStripe-int-}
```
public void setColumnStripe(int value)
```


Устанавливает количество столбцов для включения в полосу, когда стиль определяет полосу нечетных/четных столбцов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество столбцов, которые необходимо включить в полосу, когда стиль определяет полосу нечетных/четных столбцов. |

### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


Задает значение, представляющее левый отступ таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение, представляющее левый отступ таблицы. |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Задает количество места (в пунктах), добавляемого слева от содержимого ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), добавляемого слева от содержимого ячеек таблицы. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Устанавливает имя стиля.

Не может быть пустой строкой.

Если в коллекции уже есть стиль с таким именем, то этот стиль переопределит его. Все затронутые узлы будут ссылаться на новый стиль.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название стиля. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String-}
```
public void setNextParagraphStyleName(String value)
```


Получает/задает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного с использованием указанного стиля. Это свойство не используется Aspose.Words. Следующий стиль абзаца будет применяться автоматически только при редактировании документа в MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Задает количество места (в пунктах), добавляемого справа от содержимого ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить справа от содержимого ячеек таблицы. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object-}
```
public void setRowAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int-}
```
public void setRowStripe(int value)
```


Устанавливает количество строк для включения в полосу, когда стиль определяет полосу нечетных/четных строк.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество строк, которые следует включить в полосу, когда стиль указывает полосу нечетных/четных строк. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Устанавливает количество места (в пунктах) для добавления над содержимым ячеек таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Количество места (в пунктах), которое нужно добавить над содержимым ячеек таблицы. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


 Указывает вертикальное выравнивание ячеек. Значение по умолчанию[CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment\#TOP).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment) константы. |

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
