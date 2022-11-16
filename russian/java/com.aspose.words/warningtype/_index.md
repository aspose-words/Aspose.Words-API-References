---
title: WarningType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип предупреждения, выдаваемого Aspose.Words во время загрузки или сохранения документа.
type: docs
weight: 607
url: /ru/java/com.aspose.words/warningtype/
---

**Наследование:**
java.lang.Object
```
public class WarningType
```

Указывает тип предупреждения, выдаваемого Aspose.Words во время загрузки или сохранения документа.
## Поля

| Поле | Описание |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Общая потеря данных, без конкретного кода. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Некоторый текст/знак/изображение или другие данные будут отсутствовать либо в дереве документа после загрузки, либо в созданном документе после сохранения. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Потеря информации о встроенном шрифте во время сохранения документа. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Шрифт заменен. |
| [HINT](#HINT) | Сообщает о потенциальной проблеме или предлагает улучшение. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Общая основная потеря форматирования, без конкретного кода. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | Результирующий документ или определенное место в нем может существенно отличаться от исходного документа. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Общая незначительная потеря форматирования, без конкретного кода. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | Результирующий документ или определенное место в нем может выглядеть несколько иначе, чем исходный документ. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Общий неожиданный контент, без специального кода. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Некоторое содержимое в исходном документе не может быть распознано (т.е. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String warningTypeName)](#fromName-java.lang.String-) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int warningType)](#getName-int-) |  |
| [getNames(int warningType)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int warningType)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Общая потеря данных, без конкретного кода.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Некоторый текст/знак/изображение или другие данные будут отсутствовать либо в дереве документа после загрузки, либо в созданном документе после сохранения.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Потеря информации о встроенном шрифте во время сохранения документа.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Шрифт заменен.

### HINT {#HINT}
```
public static int HINT
```


Сообщает о потенциальной проблеме или предлагает улучшение.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Общая основная потеря форматирования, без конкретного кода.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


Результирующий документ или определенное место в нем может существенно отличаться от исходного документа.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Общая незначительная потеря форматирования, без конкретного кода.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


Результирующий документ или определенное место в нем может выглядеть несколько иначе, чем исходный документ.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Общий неожиданный контент, без специального кода.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Некоторый контент в исходном документе не может быть распознан (т. е. не поддерживается), это может вызвать или не вызвать проблемы или привести к потере данных/форматирования.

### length {#length}
```
public static int length
```


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
### fromName(String warningTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String warningTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set warningTypeNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int warningType) {#getName-int-}
```
public static String getName(int warningType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| warningType | int |  |

**Возвращает:**
java.lang.String
### getNames(int warningType) {#getNames-int-}
```
public static Set getNames(int warningType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| warningType | int |  |

**Возвращает:**
java.util.Set
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
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




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int warningType) {#toString-int-}
```
public static String toString(int warningType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| warningType | int |  |

**Возвращает:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

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
