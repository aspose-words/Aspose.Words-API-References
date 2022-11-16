---
title: FieldBuilder
second_title: Справочник по API Aspose.Words для Java
description: Создает поле из аргументов и переключателей токенов кода поля.
type: docs
weight: 166
url: /ru/java/com.aspose.words/fieldbuilder/
---

**Наследование:**
java.lang.Object
```
public class FieldBuilder
```

Создает поле из токенов кода поля (аргументы и переключатели).

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FieldBuilder(int fieldType)](#FieldBuilder-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [addArgument(FieldArgumentBuilder argument)](#addArgument-com.aspose.words.FieldArgumentBuilder-) |  Добавляет аргумент поля, представленный[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) к коду поля. |
| [addArgument(FieldBuilder argument)](#addArgument-com.aspose.words.FieldBuilder-) |  Добавляет дочернее поле, представленное другим[FieldBuilder](../../com.aspose.words/fieldbuilder) к коду поля. |
| [addArgument(double argument)](#addArgument-double-) | Добавляет аргумент поля. |
| [addArgument(int argument)](#addArgument-int-) | Добавляет аргумент поля. |
| [addArgument(String argument)](#addArgument-java.lang.String-) | Добавляет аргумент поля. |
| [addSwitch(String switchName)](#addSwitch-java.lang.String-) | Добавляет переключатель поля. |
| [addSwitch(String switchName, double switchArgument)](#addSwitch-java.lang.String-double-) | Добавляет переключатель поля. |
| [addSwitch(String switchName, int switchArgument)](#addSwitch-java.lang.String-int-) | Добавляет переключатель поля. |
| [addSwitch(String switchName, String switchArgument)](#addSwitch-java.lang.String-java.lang.String-) | Добавляет переключатель поля. |
| [buildAndInsert(Inline refNode)](#buildAndInsert-com.aspose.words.Inline-) | Создает и вставляет поле в документ перед указанным встроенным узлом. |
| [buildAndInsert(Paragraph refNode)](#buildAndInsert-com.aspose.words.Paragraph-) | Создает и вставляет поле в документ до конца указанного абзаца. |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder-) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FieldBuilder(int fieldType) {#FieldBuilder-int-}
```
public FieldBuilder(int fieldType)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | int |  |

### addArgument(FieldArgumentBuilder argument) {#addArgument-com.aspose.words.FieldArgumentBuilder-}
```
public FieldBuilder addArgument(FieldArgumentBuilder argument)
```


 Добавляет аргумент поля, представленный[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)к коду поля. Эта перегрузка используется, когда аргумент состоит из смеси различных частей, таких как дочерние поля, узлы и обычный текст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) |  |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(FieldBuilder argument) {#addArgument-com.aspose.words.FieldBuilder-}
```
public FieldBuilder addArgument(FieldBuilder argument)
```


 Добавляет дочернее поле, представленное другим[FieldBuilder](../../com.aspose.words/fieldbuilder) к коду поля. Эта перегрузка используется, когда аргумент состоит из одного дочернего поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | [FieldBuilder](../../com.aspose.words/fieldbuilder) |  |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(double argument) {#addArgument-double-}
```
public FieldBuilder addArgument(double argument)
```


Добавляет аргумент поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | double | Значение аргумента. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(int argument) {#addArgument-int-}
```
public FieldBuilder addArgument(int argument)
```


Добавляет аргумент поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | int | Значение аргумента. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(String argument) {#addArgument-java.lang.String-}
```
public FieldBuilder addArgument(String argument)
```


Добавляет аргумент поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| argument | java.lang.String | Значение аргумента. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName) {#addSwitch-java.lang.String-}
```
public FieldBuilder addSwitch(String switchName)
```


Добавляет переключатель поля. Эта перегрузка добавляет флаг (переключатель без аргумента).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String | Имя переключателя. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, double switchArgument) {#addSwitch-java.lang.String-double-}
```
public FieldBuilder addSwitch(String switchName, double switchArgument)
```


Добавляет переключатель поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String | Имя переключателя. |
| switchArgument | double | Значение переключателя. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, int switchArgument) {#addSwitch-java.lang.String-int-}
```
public FieldBuilder addSwitch(String switchName, int switchArgument)
```


Добавляет переключатель поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String | Имя переключателя. |
| switchArgument | int | Значение переключателя. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, String switchArgument) {#addSwitch-java.lang.String-java.lang.String-}
```
public FieldBuilder addSwitch(String switchName, String switchArgument)
```


Добавляет переключатель поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String | Имя переключателя. |
| switchArgument | java.lang.String | Значение переключателя. |

**Возвращает:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### buildAndInsert(Inline refNode) {#buildAndInsert-com.aspose.words.Inline-}
```
public Field buildAndInsert(Inline refNode)
```


Создает и вставляет поле в документ перед указанным встроенным узлом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| refNode | [Inline](../../com.aspose.words/inline) |  |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
### buildAndInsert(Paragraph refNode) {#buildAndInsert-com.aspose.words.Paragraph-}
```
public Field buildAndInsert(Paragraph refNode)
```


Создает и вставляет поле в документ до конца указанного абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| refNode | [Paragraph](../../com.aspose.words/paragraph) |  |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder-}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder) |  |

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
