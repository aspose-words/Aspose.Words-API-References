---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words لـ Java"
description: "يحدد مرشحًا لتخطي العناصر بناءً على فهارسها في Java."
type: docs
weight: 774
url: /ar/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

يحدد مرشحًا لتخطي العناصر بناءً على فهارسها.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | يحدد ما إذا كان يجب تخطي العنصر ذو الفهرس المحدد. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


يحدد ما إذا كان يجب تخطي العنصر ذو الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس العنصر. |

**Returns:**
منطقي -  true  إذا كان يجب تخطي العنصر؛ وإلا،  false .
