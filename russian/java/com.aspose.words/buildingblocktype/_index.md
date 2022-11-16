---
title: BuildingBlockType
second_title: Справочник по API Aspose.Words для Java
description: Задает тип стандартного блока.
type: docs
weight: 45
url: /ru/java/com.aspose.words/buildingblocktype/
---

**Наследование:**
java.lang.Object
```
public class BuildingBlockType
```

Задает тип стандартного блока. Тип может повлиять на видимость и поведение стандартного блока в Microsoft Word.

 Соответствует**ST\_DocPartType** введите OOXML.
## Поля

| Поле | Описание |
| --- | --- |
| [ALL](#ALL) | Строительный блок связан со всеми типами. |
| [AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT](#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT) | Позволяет автоматически вставлять стандартный блок в документ всякий раз, когда его имя вводится в приложение. |
| [AUTO_CORRECT](#AUTO-CORRECT) | Стандартный блок связан с инструментами правописания и грамматики. |
| [AUTO_TEXT](#AUTO-TEXT) | Стандартным блоком является запись автотекста. |
| [DEFAULT](#DEFAULT) |  Сохранить как[NONE](../../com.aspose.words/buildingblocktype\#NONE). |
| [FORM_FIELD_HELP_TEXT](#FORM-FIELD-HELP-TEXT) | Стандартный блок представляет собой текст справки по полю формы. |
| [NONE](#NONE) | Для стандартного блока не указывается информация о типе. |
| [NORMAL](#NORMAL) | Строительный блок является нормальным (т.е. |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) | Стандартный блок представляет собой структурированный текст-заполнитель тега документа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String buildingBlockTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int buildingBlockType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int buildingBlockType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALL {#ALL}
```
public static int ALL
```


Строительный блок связан со всеми типами.

### AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT {#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT}
```
public static int AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT
```


Позволяет автоматически вставлять стандартный блок в документ всякий раз, когда его имя вводится в приложение.

### AUTO_CORRECT {#AUTO-CORRECT}
```
public static int AUTO_CORRECT
```


Стандартный блок связан с инструментами правописания и грамматики.

### AUTO_TEXT {#AUTO-TEXT}
```
public static int AUTO_TEXT
```


Стандартным блоком является запись автотекста.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Сохранить как[NONE](../../com.aspose.words/buildingblocktype\#NONE).

### FORM_FIELD_HELP_TEXT {#FORM-FIELD-HELP-TEXT}
```
public static int FORM_FIELD_HELP_TEXT
```


Стандартный блок представляет собой текст справки по полю формы.

### NONE {#NONE}
```
public static int NONE
```


Для стандартного блока не указывается информация о типе.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Стандартный блок представляет собой обычный (т. е. обычный) элемент документа глоссария.

### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```


Стандартный блок представляет собой структурированный текст-заполнитель тега документа.

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
### fromName(String buildingBlockTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String buildingBlockTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| buildingBlockTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int buildingBlockType) {#getName-int-}
```
public static String getName(int buildingBlockType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| buildingBlockType | int |  |

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
### toString(int buildingBlockType) {#toString-int-}
```
public static String toString(int buildingBlockType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| buildingBlockType | int |  |

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
