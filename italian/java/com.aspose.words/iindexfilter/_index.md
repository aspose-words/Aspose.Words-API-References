---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words per Java"
description: "Definisce un filtro per saltare gli elementi in base ai loro indici in Java."
type: docs
weight: 774
url: /it/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

Definisce un filtro per saltare gli elementi in base ai loro indici.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | Determina se l'elemento con l'indice specificato deve essere ignorato. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


Determina se l'elemento con l'indice specificato deve essere ignorato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int | L'indice dell'elemento. |

**Returns:**
boolean -  true  se l'elemento deve essere ignorato; altrimenti,  false .
