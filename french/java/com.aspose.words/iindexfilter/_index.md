---
title: "IIndexFilter"
linktitle: "IIndexFilter"
second_title: "Aspose.Words pour Java"
description: "Définit un filtre pour ignorer les éléments en fonction de leurs indices en Java."
type: docs
weight: 774
url: /fr/java/com.aspose.words/iindexfilter/
---
```
public interface IIndexFilter
```

Définit un filtre pour ignorer les éléments en fonction de leurs indices.
## Méthodes

| Méthode | Description |
| --- | --- |
| [shouldSkipIndex(int index)](#shouldSkipIndex-int) | Détermine si l'élément avec l'index spécifié doit être ignoré. |
### shouldSkipIndex(int index) {#shouldSkipIndex-int}
```
public abstract boolean shouldSkipIndex(int index)
```


Détermine si l'élément avec l'index spécifié doit être ignoré.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | L'index de l'élément. |

**Returns:**
booléen -  vrai  si l'élément doit être ignoré ; sinon,  faux .
