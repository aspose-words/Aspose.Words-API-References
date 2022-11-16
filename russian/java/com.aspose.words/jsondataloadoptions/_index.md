---
title: JsonDataLoadOptions
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры анализа данных JSON.
type: docs
weight: 353
url: /ru/java/com.aspose.words/jsondataloadoptions/
---

**Наследование:**
java.lang.Object
```
public class JsonDataLoadOptions
```

Представляет параметры анализа данных JSON.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.

 Экземпляр этого класса может быть передан в конструкторы[JsonDataSource](../../com.aspose.words/jsondatasource).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [JsonDataLoadOptions()](#JsonDataLoadOptions--) | Инициализирует новый экземпляр этого класса с параметрами по умолчанию. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject--) | Получает флаг, указывающий, всегда ли сгенерированный источник данных будет содержать объект для корневого элемента JSON. |
| [getClass()](#getClass--) |  |
| [getExactDateTimeParseFormat()](#getExactDateTimeParseFormat--) | Получает точный формат для анализа значений даты и времени JSON при загрузке JSON. |
| [getExactDateTimeParseFormats()](#getExactDateTimeParseFormats--) | Получает точные форматы для анализа значений даты и времени JSON при загрузке JSON. |
| [getSimpleValueParseMode()](#getSimpleValueParseMode--) | Получает режим для анализа простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean-) | Устанавливает флаг, указывающий, всегда ли сгенерированный источник данных будет содержать объект для корневого элемента JSON. |
| [setExactDateTimeParseFormat(String value)](#setExactDateTimeParseFormat-java.lang.String-) | Задает точный формат для анализа значений даты и времени JSON при загрузке JSON. |
| [setExactDateTimeParseFormats(Iterable value)](#setExactDateTimeParseFormats-java.lang.Iterable-) | Задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. |
| [setSimpleValueParseMode(int value)](#setSimpleValueParseMode-int-) | Задает режим разбора простых значений JSON (пустых, логических, числовых, целых и строковых) при загрузке JSON. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### JsonDataLoadOptions() {#JsonDataLoadOptions--}
```
public JsonDataLoadOptions()
```


Инициализирует новый экземпляр этого класса с параметрами по умолчанию.

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
### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject--}
```
public boolean getAlwaysGenerateRootObject()
```


 Получает флаг, указывающий, всегда ли сгенерированный источник данных будет содержать объект для корневого элемента JSON. Если корневой элемент JSON содержит одно сложное свойство, такой объект по умолчанию не создается. Значение по умолчанию**false**.

**Возвращает:**
boolean — флаг, указывающий, всегда ли сгенерированный источник данных будет содержать объект для корневого элемента JSON.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getExactDateTimeParseFormat() {#getExactDateTimeParseFormat--}
```
public String getExactDateTimeParseFormat()
```


 Получает точный формат для анализа значений даты и времени JSON при загрузке JSON. По умолчанию**null**.

Строки, закодированные с использованием формата даты и времени Microsoft® JSON (например, «/Date(1224043200000)/»), всегда распознаются как значения даты и времени независимо от значения этого свойства. Свойство определяет дополнительные форматы, которые будут использоваться при анализе значений даты и времени из строк следующим образом:

 *   Когда[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-) является**null**, формат ISO-8601 и все форматы даты и времени, поддерживаемые для текущего языка, английского языка США и английского языка Новой Зеландии, используются дополнительно в указанном порядке.
 *   Когда[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-) — это непустая строка, она используется как единый дополнительный формат даты и времени, использующий текущий язык и региональные параметры.
 *   Когда[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-) является пустой строкой, дополнительные форматы даты и времени не используются.

**Возвращает:**
java.lang.String — точный формат для анализа значений даты и времени JSON при загрузке JSON.
### getExactDateTimeParseFormats() {#getExactDateTimeParseFormats--}
```
public Iterable getExactDateTimeParseFormats()
```


 Получает точные форматы для анализа значений даты и времени JSON при загрузке JSON. По умолчанию**null**.

Строки, закодированные с использованием формата даты и времени Microsoft® JSON (например, «/Date(1224043200000)/»), всегда распознаются как значения даты и времени независимо от значения этого свойства. Свойство определяет дополнительные форматы, которые будут использоваться при анализе значений даты и времени из строк следующим образом:

 *   Когда[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-) является**null**, формат ISO-8601 и все форматы даты и времени, поддерживаемые для текущего языка, английского языка США и английского языка Новой Зеландии, используются дополнительно в указанном порядке.
 *   Когда[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-) содержит строки, они используются как дополнительные форматы даты и времени, использующие текущий язык и региональные параметры.
 *   Когда[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-) пуст, дополнительные форматы даты и времени не используются.

**Возвращает:**
java.lang.Iterable — точные форматы для анализа значений даты и времени JSON при загрузке JSON.
### getSimpleValueParseMode() {#getSimpleValueParseMode--}
```
public int getSimpleValueParseMode()
```


 Получает режим для анализа простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. Такой режим не влияет на синтаксический анализ значений даты и времени. По умолчанию[JsonSimpleValueParseMode.LOOSE](../../com.aspose.words/jsonsimplevalueparsemode\#LOOSE).

**Возвращает:**
 int — режим разбора простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. Возвращаемое значение является одним из[JsonSimpleValueParseMode](../../com.aspose.words/jsonsimplevalueparsemode) константы.
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




### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean-}
```
public void setAlwaysGenerateRootObject(boolean value)
```


 Устанавливает флаг, указывающий, всегда ли сгенерированный источник данных будет содержать объект для корневого элемента JSON. Если корневой элемент JSON содержит одно сложное свойство, такой объект по умолчанию не создается. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, всегда ли сгенерированный источник данных будет содержать объект для корневого элемента JSON. |

### setExactDateTimeParseFormat(String value) {#setExactDateTimeParseFormat-java.lang.String-}
```
public void setExactDateTimeParseFormat(String value)
```


 Задает точный формат для анализа значений даты и времени JSON при загрузке JSON. По умолчанию**null**.

Строки, закодированные с использованием формата даты и времени Microsoft® JSON (например, «/Date(1224043200000)/»), всегда распознаются как значения даты и времени независимо от значения этого свойства. Свойство определяет дополнительные форматы, которые будут использоваться при анализе значений даты и времени из строк следующим образом:

 *   Когда[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-) является**null**, формат ISO-8601 и все форматы даты и времени, поддерживаемые для текущего языка, английского языка США и английского языка Новой Зеландии, используются дополнительно в указанном порядке.
 *   Когда[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-) — это непустая строка, она используется как единый дополнительный формат даты и времени, использующий текущий язык и региональные параметры.
 *   Когда[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-) является пустой строкой, дополнительные форматы даты и времени не используются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Точный формат для анализа значений даты и времени JSON при загрузке JSON. |

### setExactDateTimeParseFormats(Iterable value) {#setExactDateTimeParseFormats-java.lang.Iterable-}
```
public void setExactDateTimeParseFormats(Iterable value)
```


Задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. По умолчанию**null**.

Строки, закодированные с использованием формата даты и времени Microsoft® JSON (например, «/Date(1224043200000)/»), всегда распознаются как значения даты и времени независимо от значения этого свойства. Свойство определяет дополнительные форматы, которые будут использоваться при анализе значений даты и времени из строк следующим образом:

 *   Когда[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-) является**null**, формат ISO-8601 и все форматы даты и времени, поддерживаемые для текущего языка, английского языка США и английского языка Новой Зеландии, используются дополнительно в указанном порядке.
 *   Когда[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-) содержит строки, они используются как дополнительные форматы даты и времени, использующие текущий язык и региональные параметры.
 *   Когда[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-) пуст, дополнительные форматы даты и времени не используются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Iterable | Точные форматы для анализа значений даты и времени JSON при загрузке JSON. |

### setSimpleValueParseMode(int value) {#setSimpleValueParseMode-int-}
```
public void setSimpleValueParseMode(int value)
```


 Задает режим разбора простых значений JSON (пустых, логических, числовых, целых и строковых) при загрузке JSON. Такой режим не влияет на синтаксический анализ значений даты и времени. По умолчанию[JsonSimpleValueParseMode.LOOSE](../../com.aspose.words/jsonsimplevalueparsemode\#LOOSE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Режим анализа простых значений JSON (пустых, логических, числовых, целых и строковых) при загрузке JSON. Значение должно быть одним из[JsonSimpleValueParseMode](../../com.aspose.words/jsonsimplevalueparsemode) константы. |

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
