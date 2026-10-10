---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words для Java"
description: "Определяет фильтр для пропуска элементов на основе их индексов в Java."
type: docs
weight: 774
url: /ru/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

Определяет фильтр для пропуска элементов на основе их индексов.
## Методы

| Метод | Описание |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | Определяет, следует ли пропустить элемент с указанным индексом. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


Определяет, следует ли пропустить элемент с указанным индексом.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс элемента. |

**Returns:**
boolean -  true  если элемент следует пропустить; иначе,  false .
