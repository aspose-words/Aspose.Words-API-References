---
title: SdtType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип узла SDT тега структурированного документа.
type: docs
weight: 508
url: /ru/java/com.aspose.words/sdttype/
---

**Наследование:**
java.lang.Object
```
public class SdtType
```

Задает тип узла тега структурированного документа (SDT).
## Поля

| Поле | Описание |
| --- | --- |
| [BIBLIOGRAPHY](#BIBLIOGRAPHY) | SDT представляет собой библиографическую запись. |
| [BUILDING_BLOCK_GALLERY](#BUILDING-BLOCK-GALLERY) | SDT представляет тип галереи стандартных блоков. |
| [CHECKBOX](#CHECKBOX) | SDT представляет собой флажок при отображении в документе. |
| [CITATION](#CITATION) | SDT представляет собой цитату. |
| [COMBO_BOX](#COMBO-BOX) | SDT представляет собой поле со списком при отображении в документе. |
| [DATE](#DATE) | SDT представляет собой средство выбора даты при отображении в документе. |
| [DOC_PART_OBJ](#DOC-PART-OBJ) | SDT представляет тип части документа. |
| [DROP_DOWN_LIST](#DROP-DOWN-LIST) | SDT представляет собой раскрывающийся список при отображении в документе. |
| [ENTITY_PICKER](#ENTITY-PICKER) | SDT представляет средство выбора объектов, которое позволяет пользователю выбирать экземпляр внешнего типа контента. |
| [EQUATION](#EQUATION) | SDT представляет собой уравнение. |
| [GROUP](#GROUP) | SDT представляет ограниченную группу при отображении в документе. |
| [NONE](#NONE) | Тип SDT не назначается. |
| [PICTURE](#PICTURE) | SDT представляет изображение при отображении в документе. |
| [PLAIN_TEXT](#PLAIN-TEXT) | SDT представляет собой обычное текстовое поле при отображении в документе. |
| [REPEATING_SECTION](#REPEATING-SECTION) | SDT представляет тип повторяющегося раздела при отображении в документе. |
| [REPEATING_SECTION_ITEM](#REPEATING-SECTION-ITEM) | SDT представляет повторяющийся элемент раздела. |
| [RICH_TEXT](#RICH-TEXT) | SDT представляет собой форматированное текстовое поле при отображении в документе. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String sdtTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int sdtType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int sdtType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BIBLIOGRAPHY {#BIBLIOGRAPHY}
```
public static int BIBLIOGRAPHY
```


SDT представляет собой библиографическую запись.

### BUILDING_BLOCK_GALLERY {#BUILDING-BLOCK-GALLERY}
```
public static int BUILDING_BLOCK_GALLERY
```


SDT представляет тип галереи стандартных блоков.

### CHECKBOX {#CHECKBOX}
```
public static int CHECKBOX
```


SDT представляет собой флажок при отображении в документе. Это специфичная для MS функция, доступная начиная с Office 2010 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### CITATION {#CITATION}
```
public static int CITATION
```


SDT представляет собой цитату.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


SDT представляет собой поле со списком при отображении в документе.

### DATE {#DATE}
```
public static int DATE
```


SDT представляет собой средство выбора даты при отображении в документе.

### DOC_PART_OBJ {#DOC-PART-OBJ}
```
public static int DOC_PART_OBJ
```


SDT представляет тип части документа.

### DROP_DOWN_LIST {#DROP-DOWN-LIST}
```
public static int DROP_DOWN_LIST
```


SDT представляет собой раскрывающийся список при отображении в документе.

### ENTITY_PICKER {#ENTITY-PICKER}
```
public static int ENTITY_PICKER
```


SDT представляет средство выбора объектов, которое позволяет пользователю выбирать экземпляр внешнего типа контента. Это специфичная для MS функция, доступная начиная с Office 2010 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### EQUATION {#EQUATION}
```
public static int EQUATION
```


SDT представляет собой уравнение.

### GROUP {#GROUP}
```
public static int GROUP
```


SDT представляет ограниченную группу при отображении в документе.

### NONE {#NONE}
```
public static int NONE
```


Тип SDT не назначается.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


SDT представляет изображение при отображении в документе.

### PLAIN_TEXT {#PLAIN-TEXT}
```
public static int PLAIN_TEXT
```


SDT представляет собой обычное текстовое поле при отображении в документе.

### REPEATING_SECTION {#REPEATING-SECTION}
```
public static int REPEATING_SECTION
```


SDT представляет тип повторяющегося раздела при отображении в документе. Это специфичная для MS функция, доступная начиная с Office 2013 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### REPEATING_SECTION_ITEM {#REPEATING-SECTION-ITEM}
```
public static int REPEATING_SECTION_ITEM
```


SDT представляет повторяющийся элемент раздела. Это специфичная для MS функция, доступная начиная с Office 2013 и не поддерживаемая стандартом ISO/IEC 29500 OOXML.

### RICH_TEXT {#RICH-TEXT}
```
public static int RICH_TEXT
```


SDT представляет собой форматированное текстовое поле при отображении в документе.

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
### fromName(String sdtTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String sdtTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int sdtType) {#getName-int-}
```
public static String getName(int sdtType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtType | int |  |

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
### toString(int sdtType) {#toString-int-}
```
public static String toString(int sdtType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtType | int |  |

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
