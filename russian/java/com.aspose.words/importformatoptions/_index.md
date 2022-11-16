---
title: ImportFormatOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать различные параметры импорта для форматирования вывода.
type: docs
weight: 347
url: /ru/java/com.aspose.words/importformatoptions/
---

**Наследование:**
java.lang.Object
```
public class ImportFormatOptions
```

Позволяет указать различные параметры импорта для форматирования вывода.

 Чтобы узнать больше, посетите**Specify Load Options** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getForceCopyStyles()](#getForceCopyStyles--) |  Получает логическое значение, указывающее либо копировать конфликтующие стили в[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) режим. |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter--) |  Получает логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes--) |  Получает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. |
| [getKeepSourceNumbering()](#getKeepSourceNumbering--) | Получает логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. |
| [getMergePastedLists()](#getMergePastedLists--) | Получает логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior--) | Получает логическое значение, указывающее, как будут импортироваться стили, если они имеют одинаковые имена в исходном и целевом документах. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean-) |  Задает логическое значение, указывающее либо копировать конфликтующие стили в[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) режим. |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean-) |  Задает логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean-) |  Задает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean-) | Задает логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean-) | Задает логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean-) | Задает логическое значение, указывающее, как будут импортироваться стили, если они имеют одинаковые имена в исходном и целевом документах. |
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
### getForceCopyStyles() {#getForceCopyStyles--}
```
public boolean getForceCopyStyles()
```


 Получает логическое значение, указывающее либо копировать конфликтующие стили в[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)режим. Значение по умолчанию неверно .

По умолчанию, если соответствующий стиль уже существует в целевом документе, форматирование исходного стиля расширяется до атрибутов прямого узла, а стиль этого узла сбрасывается до значения по умолчанию.

Если для этого параметра установлено значение true, исходный стиль будет принудительно скопирован в целевой документ с уникальным именем и применен к импортированному узлу.

Обратите внимание, в этом случае не гарантируется сохранение форматирования импортируемого узла в целевом документе.

**Возвращает:**
 boolean — логическое значение, указывающее либо копировать конфликтующие стили в[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) режим.
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter--}
```
public boolean getIgnoreHeaderFooter()
```


 Получает логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. Значение по умолчанию верно .

**Возвращает:**
 boolean — логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим.
### getIgnoreTextBoxes() {#getIgnoreTextBoxes--}
```
public boolean getIgnoreTextBoxes()
```


 Получает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. Значение по умолчанию верно .

**Возвращает:**
 boolean — логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим.
### getKeepSourceNumbering() {#getKeepSourceNumbering--}
```
public boolean getKeepSourceNumbering()
```


Получает логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. Значение по умолчанию неверно .

**Возвращает:**
boolean — логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах.
### getMergePastedLists() {#getMergePastedLists--}
```
public boolean getMergePastedLists()
```


Получает логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию неверно .

**Возвращает:**
boolean — логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками.
### getSmartStyleBehavior() {#getSmartStyleBehavior--}
```
public boolean getSmartStyleBehavior()
```


Получает логическое значение, указывающее, как будут импортироваться стили, если они имеют одинаковые имена в исходном и целевом документах. Значение по умолчанию неверно .

 Когда этот вариант**enabled** , исходный стиль будет развернут в прямые атрибуты внутри целевого документа, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим импорта.

 Когда этот вариант**disabled**, исходный стиль будет развернут, только если он пронумерован. Существующие атрибуты назначения не будут переопределены, включая списки.

**Возвращает:**
boolean — логическое значение, указывающее, как будут импортироваться стили, если они имеют одинаковые имена в исходном и целевом документах.
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




### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean-}
```
public void setForceCopyStyles(boolean value)
```


 Задает логическое значение, указывающее либо копировать конфликтующие стили в[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING)режим. Значение по умолчанию неверно .

По умолчанию, если соответствующий стиль уже существует в целевом документе, форматирование исходного стиля расширяется до атрибутов прямого узла, а стиль этого узла сбрасывается до значения по умолчанию.

Если для этого параметра установлено значение true, исходный стиль будет принудительно скопирован в целевой документ с уникальным именем и применен к импортированному узлу.

Обратите внимание, в этом случае не гарантируется сохранение форматирования импортируемого узла в целевом документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее либо копировать конфликтующие стили в[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) режим. |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean-}
```
public void setIgnoreHeaderFooter(boolean value)
```


 Задает логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Логическое значение, указывающее, что исходное форматирование содержимого верхних и нижних колонтитулов игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean-}
```
public void setIgnoreTextBoxes(boolean value)
```


 Задает логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Логическое значение, указывающее, что исходное форматирование содержимого текстовых полей игнорируется, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим. |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean-}
```
public void setKeepSourceNumbering(boolean value)
```


Задает логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, как будет импортироваться нумерация, если она конфликтует в исходном и целевом документах. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean-}
```
public void setMergePastedLists(boolean value)
```


Задает логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, будут ли вставленные списки объединяться с окружающими списками. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean-}
```
public void setSmartStyleBehavior(boolean value)
```


Задает логическое значение, указывающее, как будут импортироваться стили, если они имеют одинаковые имена в исходном и целевом документах. Значение по умолчанию неверно .

 Когда этот вариант**enabled** , исходный стиль будет развернут в прямые атрибуты внутри целевого документа, если[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode\#KEEP-SOURCE-FORMATTING) используется режим импорта.

 Когда этот вариант**disabled**, исходный стиль будет развернут, только если он пронумерован. Существующие атрибуты назначения не будут переопределены, включая списки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, как будут импортироваться стили, если они имеют одинаковые имена в исходном и целевом документах. |

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
