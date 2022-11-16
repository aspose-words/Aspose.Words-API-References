---
title: CsvDataLoadOptions
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры анализа данных CSV.
type: docs
weight: 98
url: /ru/java/com.aspose.words/csvdataloadoptions/
---

**Наследование:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Представляет параметры анализа данных CSV.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.

 Экземпляр этого класса может быть передан в конструкторы[CsvDataSource](../../com.aspose.words/csvdatasource).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions--) | Инициализирует новый экземпляр этого класса с параметрами по умолчанию. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean-) | Инициализирует новый экземпляр этого класса, указывая, содержат ли данные CSV имена столбцов в первой строке. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCommentChar()](#getCommentChar--) | Получает символ, используемый для комментирования строк данных CSV. |
| [getDelimiter()](#getDelimiter--) | Получает символ, который будет использоваться в качестве разделителя столбцов. |
| [getQuoteChar()](#getQuoteChar--) | Получает символ, используемый для кавычек значений поля. |
| [hasHeaders()](#hasHeaders--) | Получает значение, указывающее, содержит ли первая запись данных CSV имена столбцов. |
| [hasHeaders(boolean value)](#hasHeaders-boolean-) | Задает значение, указывающее, содержит ли первая запись данных CSV имена столбцов. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCommentChar(char value)](#setCommentChar-char-) | Задает символ, используемый для комментирования строк данных CSV. |
| [setDelimiter(char value)](#setDelimiter-char-) | Устанавливает символ, который будет использоваться в качестве разделителя столбца. |
| [setQuoteChar(char value)](#setQuoteChar-char-) | Задает символ, который используется для кавычек значений поля. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CsvDataLoadOptions() {#CsvDataLoadOptions--}
```
public CsvDataLoadOptions()
```


Инициализирует новый экземпляр этого класса с параметрами по умолчанию.

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean-}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


Инициализирует новый экземпляр этого класса, указывая, содержат ли данные CSV имена столбцов в первой строке.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| hasHeaders | boolean |  |

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
### getCommentChar() {#getCommentChar--}
```
public char getCommentChar()
```


Получает символ, используемый для комментирования строк данных CSV. Значение по умолчанию: '\#' (цифровой знак).

**Возвращает:**
char — символ, который используется для комментирования строк данных CSV.
### getDelimiter() {#getDelimiter--}
```
public char getDelimiter()
```


Получает символ, который будет использоваться в качестве разделителя столбцов. Значение по умолчанию — ',' (запятая).

**Возвращает:**
char — символ, который будет использоваться в качестве разделителя столбцов.
### getQuoteChar() {#getQuoteChar--}
```
public char getQuoteChar()
```


Получает символ, используемый для кавычек значений поля.

Значение по умолчанию — '"' (кавычки).

Удвойте символ, чтобы поместить его в цитируемый текст.

**Возвращает:**
char — символ, который используется для кавычек значений поля.
### hasHeaders() {#hasHeaders--}
```
public boolean hasHeaders()
```


 Получает значение, указывающее, содержит ли первая запись данных CSV имена столбцов. Значение по умолчанию**false**.

**Возвращает:**
boolean — значение, указывающее, содержит ли первая запись данных CSV имена столбцов.
### hasHeaders(boolean value) {#hasHeaders-boolean-}
```
public void hasHeaders(boolean value)
```


 Задает значение, указывающее, содержит ли первая запись данных CSV имена столбцов. Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, содержит ли первая запись данных CSV имена столбцов. |

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




### setCommentChar(char value) {#setCommentChar-char-}
```
public void setCommentChar(char value)
```


Задает символ, используемый для комментирования строк данных CSV. Значение по умолчанию: '\#' (цифровой знак).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | char | Символ, используемый для комментирования строк данных CSV. |

### setDelimiter(char value) {#setDelimiter-char-}
```
public void setDelimiter(char value)
```


Устанавливает символ, который будет использоваться в качестве разделителя столбца. Значение по умолчанию — ',' (запятая).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | char | Символ, который будет использоваться в качестве разделителя столбцов. |

### setQuoteChar(char value) {#setQuoteChar-char-}
```
public void setQuoteChar(char value)
```


Задает символ, который используется для кавычек значений поля.

Значение по умолчанию — '"' (кавычки).

Удвойте символ, чтобы поместить его в цитируемый текст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | char | Символ, который используется для кавычек значений поля. |

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
