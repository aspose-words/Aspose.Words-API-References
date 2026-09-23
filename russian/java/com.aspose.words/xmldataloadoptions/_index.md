---
title: "XmlDataLoadOptions"
linktitle: "XmlDataLoadOptions"
second_title: "Aspose.Words для Java"
description: "Представляет параметры загрузки XML-данных в Java."
type: docs
weight: 745
url: /ru/java/com.aspose.words/xmldataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataLoadOptions
```

Представляет параметры загрузки XML-данных.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Экземпляр этого класса может быть передан в конструкторы [XmlDataSource](../../com.aspose.words/xmldatasource/).


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [XmlDataLoadOptions()](#XmlDataLoadOptions) | Инициализирует новый экземпляр этого класса с параметрами по умолчанию. |
## Методы

| Метод | Описание |
| --- | --- |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject) | Получает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для корневого элемента XML. |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean) | Устанавливает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для корневого элемента XML. |
### XmlDataLoadOptions() {#XmlDataLoadOptions}
```
public XmlDataLoadOptions()
```


Инициализирует новый экземпляр этого класса с параметрами по умолчанию.

### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject}
```
public boolean getAlwaysGenerateRootObject()
```


Получает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для корневого элемента XML. Если у корневого элемента XML нет атрибутов и все его дочерние элементы имеют одинаковые имена, такой объект по умолчанию не создаётся.

 **Remarks:** 

Значение по умолчанию — false.

**Returns:**
boolean — Флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для корневого элемента XML.
### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean}
```
public void setAlwaysGenerateRootObject(boolean value)
```


Устанавливает флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для корневого элемента XML. Если у корневого элемента XML нет атрибутов и все его дочерние элементы имеют одинаковые имена, такой объект по умолчанию не создаётся.

 **Remarks:** 

Значение по умолчанию — false.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, будет ли сгенерированный источник данных всегда содержать объект для корневого элемента XML. |

