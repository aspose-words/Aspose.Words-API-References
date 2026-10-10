---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words pour Java"
description: "Une interface d'une usine pour créer des implémentations ITextShaper en Java."
type: docs
weight: 787
url: /fr/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

Une interface d'une usine pour créer des implémentations [ITextShaper](../../com.aspose.words/itextshaper/).
## Méthodes

| Méthode | Description |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | Renvoie une nouvelle instance d'un text shaper pour la police représentée par  fontBlob  et  faceIndex . |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | Renvoie une nouvelle instance d'un text shaper pour la police spécifiée par  fontPath  et  faceIndex . |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Renvoie une nouvelle instance d'un text shaper pour la police représentée par  fontBlob  et  faceIndex .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontId | java.lang.String | Un identifiant unique qui peut être associé de manière unique à la police fournie fontBlob. |
| fontBlob | byte[] | Tableau d'octets contenant les données de la police. |
| faceIndex | int | Un indice de la police dans la collection de polices TrueType, ou 0 si  fontBlob  n'est pas une collection de polices TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Renvoie une nouvelle instance d'un text shaper pour la police spécifiée par  fontPath  et  faceIndex .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontPath | java.lang.String | Un chemin absolu vers le fichier de police. |
| faceIndex | int | Un indice de la police dans la collection de polices TrueType, ou 0 si le fichier de police spécifié n'est pas une collection de polices TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
