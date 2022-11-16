---
title: IFieldResultFormatter
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если хотите управлять форматированием результата поля.
type: docs
weight: 642
url: /ru/java/com.aspose.words/ifieldresultformatter/
---
```
public interface IFieldResultFormatter
```

Реализуйте этот интерфейс, если хотите управлять форматированием результата поля.
## Методы

| Метод | Описание |
| --- | --- |
| [format(double value, int format)](#format-double-int-) |  |
| [format(String value, int format)](#format-java.lang.String-int-) |  |
| [formatDateTime(Date value, String format, int calendarType)](#formatDateTime-java.util.Date-java.lang.String-int-) |  |
| [formatNumeric(double value, String format)](#formatNumeric-double-java.lang.String-) | Вызывается, когда Aspose.Words применяет переключатель числового формата, т.е. |
### format(double value, int format) {#format-double-int-}
```
public abstract String format(double value, int format)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |
| format | int |  |

**Возвращает:**
java.lang.String
### format(String value, int format) {#format-java.lang.String-int-}
```
public abstract String format(String value, int format)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  |
| format | int |  |

**Возвращает:**
java.lang.String
### formatDateTime(Date value, String format, int calendarType) {#formatDateTime-java.util.Date-java.lang.String-int-}
```
public abstract String formatDateTime(Date value, String format, int calendarType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date |  |
| format | java.lang.String |  |
| calendarType | int |  |

**Возвращает:**
java.lang.String
### formatNumeric(double value, String format) {#formatNumeric-double-java.lang.String-}
```
public abstract String formatNumeric(double value, String format)
```


Вызывается, когда Aspose.Words применяет переключатель числового формата, т.е.\\\# "\#.\ #". Реализация должна вернуть**null** чтобы указать, что форматирование по умолчанию должно быть применено.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |
| format | java.lang.String |  |

**Возвращает:**
java.lang.String