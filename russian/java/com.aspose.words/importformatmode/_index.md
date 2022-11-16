---
title: ImportFormatMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как форматирование объединяется при импорте содержимого из другого документа.
type: docs
weight: 346
url: /ru/java/com.aspose.words/importformatmode/
---

**Наследование:**
java.lang.Object
```
public class ImportFormatMode
```

Указывает, как форматирование объединяется при импорте содержимого из другого документа.

При копировании узлов из одного документа в другой этот параметр указывает, как разрешается форматирование, когда оба документа имеют стиль с одинаковым именем, но разным форматированием.

Форматирование решается следующим образом:

1.  Встроенные стили сопоставляются с использованием идентификатора стиля, независимого от языкового стандарта. Определенные пользователем стили сопоставляются с использованием имени стиля с учетом регистра.
2.  Если соответствующий стиль не найден в целевом документе, стиль (и все стили, на которые он ссылается) копируется в целевой документ, а импортированные узлы обновляются для ссылки на новый стиль.
3.   Если соответствующий стиль уже существует в целевом документе, то, что происходит, зависит от параметра importFormatMode, переданного в**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** как описано ниже.

 При использовании**UseDestinationStyles** вариант, если соответствующий стиль уже существует в целевом документе, стиль не копируется, а импортированные узлы обновляются для ссылки на существующий стиль.

 Недостаток использования**UseDestinationStyles**заключается в том, что импортированный текст может выглядеть в целевом документе иначе, чем в исходном документе. Например, стиль «Заголовок 1» в исходном документе использует шрифт Arial 16pt, а стиль «Заголовок 1» в целевом документе использует шрифт Times New Roman 14pt. При импорте текста в стиле «Заголовок 1» без другого прямого форматирования он будет отображаться в целевом документе как шрифт Times New Roman 14pt.

**KeepSourceFormatting**Параметр позволяет убедиться, что импортированное содержимое выглядит в целевом документе так же, как и в исходном документе. Если соответствующий стиль уже существует в целевом документе, форматирование исходного стиля расширяется до непосредственных атрибутов узла, а стиль изменяется на Обычный. Если стиль не существует в целевом документе, исходный стиль импортируется в целевой документ и применяется к импортированному узлу. Обратите внимание, что не всегда возможно сохранить исходный стиль, даже если он не существует в целевом документе. В этом случае форматирование такого стиля будет расширено на непосредственные атрибуты узла в пользу сохранения исходного форматирования узла.

 Недостаток использования**KeepSourceFormatting** заключается в том, что если вы выполните несколько импортов, вы можете получить много стилей в целевом документе, и это может затруднить использование согласованного форматирования стилей в Microsoft Word для этого документа.

 С использованием**KeepDifferentStyles**Опция позволяет повторно использовать конечные стили, если предоставляемое ими форматирование идентично стилям в исходном документе. Если стиль в целевом документе отличается от исходного, он импортируется.

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Поля

| Поле | Описание |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Копируйте только те стили, которые отличаются от тех, что в исходном документе. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Скопируйте все необходимые стили в конечный документ, при необходимости создайте уникальные имена стилей. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Используйте стили целевого документа и скопируйте новые стили. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String importFormatModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int importFormatMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int importFormatMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Копируйте только те стили, которые отличаются от тех, что в исходном документе.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Скопируйте все необходимые стили в конечный документ, при необходимости создайте уникальные имена стилей.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Используйте стили целевого документа и скопируйте новые стили. Это опция по умолчанию.

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
### fromName(String importFormatModeName) {#fromName-java.lang.String-}
```
public static int fromName(String importFormatModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int importFormatMode) {#getName-int-}
```
public static String getName(int importFormatMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| importFormatMode | int |  |

**Возвращает:**
java.lang.String
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
### toString(int importFormatMode) {#toString-int-}
```
public static String toString(int importFormatMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| importFormatMode | int |  |

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
