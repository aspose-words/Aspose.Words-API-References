---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words for Java"
description: "定义基于 Java 中索引的跳过项的过滤器。"
type: docs
weight: 774
url: /zh/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

定义基于索引的跳过项的过滤器。
## 方法

| 方法 | 描述 |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | 确定是否应跳过具有指定索引的项。 |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


确定是否应跳过具有指定索引的项。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int | 该项的索引。 |

**Returns:**
布尔型 - 如果应跳过该项则为 true；否则为 false。
