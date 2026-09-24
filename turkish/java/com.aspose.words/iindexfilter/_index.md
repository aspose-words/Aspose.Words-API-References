---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words Java için"
description: "Java'da indekslerine göre öğeleri atlamak için bir filtre tanımlar."
type: docs
weight: 774
url: /tr/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

Ögeleri indekslerine göre atlamak için bir filtre tanımlar.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | Belirtilen indeksli öğenin atlanıp atlanmayacağını belirler. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


Belirtilen indeksli öğenin atlanıp atlanmayacağını belirler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Öğenin indeksi. |

**Returns:**
boolean -  true  öğenin atlanması gerekiyorsa; aksi takdirde  false .
