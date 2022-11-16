---
title: FieldArgumentBuilder
second_title: Справочник по API Aspose.Words для Java
description: Создает сложный аргумент поля, состоящий из узлов полей и обычного текста.
type: docs
weight: 155
url: /ru/java/com.aspose.words/fieldargumentbuilder/
---

**Наследование:**
java.lang.Object
```
public class FieldArgumentBuilder
```

Создает сложный аргумент поля, состоящий из полей, узлов и простого текста.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FieldArgumentBuilder()](#FieldArgumentBuilder--) |  Инициализирует экземпляр[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) учебный класс. |
## Методы

| Метод | Описание |
| --- | --- |
| [addField(FieldBuilder fieldBuilder)](#addField-com.aspose.words.FieldBuilder-) |  Добавляет поле, представленное[FieldBuilder](../../com.aspose.words/fieldbuilder) к аргументу. |
| [addNode(Inline node)](#addNode-com.aspose.words.Inline-) | Добавляет узел к аргументу. |
| [addText(String text)](#addText-java.lang.String-) | Добавляет простой текст к аргументу. |
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
### FieldArgumentBuilder() {#FieldArgumentBuilder--}
```
public FieldArgumentBuilder()
```


 Инициализирует экземпляр[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) учебный класс.

### addField(FieldBuilder fieldBuilder) {#addField-com.aspose.words.FieldBuilder-}
```
public FieldArgumentBuilder addField(FieldBuilder fieldBuilder)
```


 Добавляет поле, представленное[FieldBuilder](../../com.aspose.words/fieldbuilder) к аргументу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldBuilder | [FieldBuilder](../../com.aspose.words/fieldbuilder) |  |

**Возвращает:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)
### addNode(Inline node) {#addNode-com.aspose.words.Inline-}
```
public FieldArgumentBuilder addNode(Inline node)
```


Добавляет узел к аргументу. На данный момент поддерживаются только узлы текстового уровня.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Inline](../../com.aspose.words/inline) |  |

**Возвращает:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)
### addText(String text) {#addText-java.lang.String-}
```
public FieldArgumentBuilder addText(String text)
```


Добавляет простой текст к аргументу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String |  |

**Возвращает:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)
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
