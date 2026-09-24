---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words para Java"
description: "Define un filtro para omitir elementos basados en sus índices en Java."
type: docs
weight: 774
url: /es/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

Define un filtro para omitir elementos basados en sus índices.
## Métodos

| Método | Descripción |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | Determina si el elemento con el índice especificado debe omitirse. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


Determina si el elemento con el índice especificado debe omitirse.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice del elemento. |

**Returns:**
boolean -  true  si el elemento debe omitirse; de lo contrario,  false .
