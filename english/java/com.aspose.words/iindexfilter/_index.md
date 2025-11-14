---
title: IIndexFilter
linktitle: IIndexFilter
second_title: Aspose.Words for Java
description: Defines a filter for skipping items based on their indices in Java.
type: docs
weight: 771
url: /java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

Defines a filter for skipping items based on their indices.
## Methods

| Method | Description |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | Determines whether the item with the specified index should be skipped. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


Determines whether the item with the specified index should be skipped.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The index of the item. |

**Returns:**
boolean -  true  if the item should be skipped; otherwise,  false .
