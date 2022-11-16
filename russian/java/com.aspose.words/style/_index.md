---
title: Style
second_title: Справочник по API Aspose.Words для Java
description: Представляет один встроенный или определяемый пользователем стиль.
type: docs
weight: 536
url: /ru/java/com.aspose.words/style/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class Style implements Cloneable
```

Представляет один встроенный или определяемый пользователем стиль.

 Чтобы узнать больше, посетите**Working with Styles and Themes** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Style style)](#equals-com.aspose.words.Style-) | Сравнивается с указанным стилем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getAliases()](#getAliases--) | Получает все псевдонимы этого стиля. |
| [getBaseStyleName()](#getBaseStyleName--) | Получает/задает имя стиля, на котором основан этот стиль. |
| [getBuiltIn()](#getBuiltIn--) | Истинно, если этот стиль является одним из встроенных стилей в MS Word. |
| [getClass()](#getClass--) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ владельца. |
| [getFont()](#getFont--) | Получает форматирование символов стиля. |
| [getLinkedStyleName()](#getLinkedStyleName--) | Получает имя стиля, связанного с этим. |
| [getList()](#getList--) | Получает список, определяющий форматирование этого стиля списка. |
| [getListFormat()](#getListFormat--) | Предоставляет доступ к свойствам форматирования списка стиля абзаца. |
| [getName()](#getName--) | Получает имя стиля. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName--) | Получает/задает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного с использованием указанного стиля. |
| [getParagraphFormat()](#getParagraphFormat--) | Получает форматирование абзаца стиля. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Получает независимый от языкового стандарта идентификатор стиля для встроенного стиля. |
| [getStyles()](#getStyles--) | Получает коллекцию стилей, к которым принадлежит этот стиль. |
| [getType()](#getType--) | Получает тип стиля (абзац или символ). |
| [hashCode()](#hashCode--) |  |
| [isHeading()](#isHeading--) | True, если стиль является одним из встроенных стилей заголовков. |
| [isQuickStyle()](#isQuickStyle--) | Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean-) | Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет указанный стиль из документа. |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String-) | Получает/задает имя стиля, на котором основан этот стиль. |
| [setName(String value)](#setName-java.lang.String-) | Устанавливает имя стиля. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String-) | Получает/задает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца, отформатированного с использованием указанного стиля. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
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
### getAliases() {#getAliases--}
```
public String[] getAliases()
```


Получает все псевдонимы этого стиля. Если стиль не имеет псевдонимов, то возвращается пустой массив строк.

**Возвращает:**
java.lang.String[] - Все псевдонимы этого стиля.
### getBaseStyleName() {#getBaseStyleName--}
```
public String getBaseStyleName()
```


Получает/задает имя стиля, на котором основан этот стиль. Это будет пустая строка, если стиль не основан ни на каком другом стиле и может быть установлен в пустую строку.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getBuiltIn() {#getBuiltIn--}
```
public boolean getBuiltIn()
```


Истинно, если этот стиль является одним из встроенных стилей в MS Word.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
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
### getType() {#getType--}
```
public int getType()
```


Получает тип стиля (абзац или символ).

**Возвращает:**
 int - Тип стиля (абзац или символ). Возвращаемое значение является одним из[StyleType](../../com.aspose.words/styletype) константы.
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

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String-}
```
public void setBaseStyleName(String value)
```


Получает/задает имя стиля, на котором основан этот стиль. Это будет пустая строка, если стиль не основан ни на каком другом стиле и может быть установлен в пустую строку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
