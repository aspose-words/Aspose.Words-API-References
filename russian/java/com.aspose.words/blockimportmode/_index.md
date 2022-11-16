---
title: BlockImportMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как свойства элементов уровня блока импортируются из документов на основе HTML.
type: docs
weight: 29
url: /ru/java/com.aspose.words/blockimportmode/
---

**Наследование:**
java.lang.Object
```
public class BlockImportMode
```

Указывает, как свойства элементов уровня блока импортируются из документов на основе HTML.
## Поля

| Поле | Описание |
| --- | --- |
| [MERGE](#MERGE) | Свойства родительских блоков объединяются и сохраняются в дочерних элементах (т.е. |
| [PRESERVE](#PRESERVE) | Свойства родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String blockImportModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int blockImportMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int blockImportMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Свойства родительских блоков объединяются и сохраняются в дочерних элементах (например, в абзацах или таблицах).

Свойства родительских блоков объединяются следующим образом: поля складываются вместе; границы блоков более высокого уровня отбрасываются, и сохраняются только границы самого внутреннего уровня. В результате при указании этого режима будет потеряно некоторое форматирование блоков исходного документа.

С другой стороны, поскольку все объединенные свойства уровня блока хранятся в узлах документа, все форматирование в результирующем документе будет доступно для модификации.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Свойства родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа.

Импортируются только поля и границы HTML-элементов body, div и blockquote. Свойства каждого элемента HTML хранятся отдельно.

Этот режим позволяет лучше сохранить границы и поля, видимые в документе HTML, и получить лучшие результаты преобразования. Недостатком является то, что результирующий документ становится сложнее модифицировать, так как границы и поля, хранящиеся в логической структуре, недоступны для редактирования.

Этот режим имитирует поведение MS Word в отношении импорта свойств блока.

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
### fromName(String blockImportModeName) {#fromName-java.lang.String-}
```
public static int fromName(String blockImportModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int blockImportMode) {#getName-int-}
```
public static String getName(int blockImportMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| blockImportMode | int |  |

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
### toString(int blockImportMode) {#toString-int-}
```
public static String toString(int blockImportMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| blockImportMode | int |  |

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
