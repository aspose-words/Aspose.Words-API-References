---
title: ITextShaperFactory.GetTextShaper
second_title: Référence de l'API Aspose.Words pour .NET
description: ITextShaperFactory méthode. Renvoie une nouvelle instance dun façonneur de texte pour la police spécifiée parfontPath etfaceIndex .
type: docs
weight: 10
url: /fr/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(string, int) {#gettextshaper_1}

Renvoie une nouvelle instance d'un façonneur de texte pour la police spécifiée par*fontPath* et*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fontPath | String | Un chemin absolu vers le fichier de police. |
| faceIndex | Int32 | Un index de la police dans la collection de polices TrueType, ou 0 si le fichier de police spécifié n'est pas une collection de polices TrueType. |

### Voir également

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* espace de noms [Aspose.Words.Shaping](../../itextshaperfactory/)
* Assemblée [Aspose.Words](../../../)

---

## GetTextShaper(string, byte[], int) {#gettextshaper}

Renvoie une nouvelle instance d'un façonneur de texte pour la police représentée par*fontBlob* et*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fontId | String | Un identifiant unique qui peut être associé de manière unique à la police fournie*fontBlob* . |
| fontBlob | Byte[] | Tableau d'octets avec les données de police. |
| faceIndex | Int32 | Un index de la police dans la collection de polices TrueType, ou 0 si*fontBlob* n'est pas une collection de polices TrueType. |

### Voir également

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* espace de noms [Aspose.Words.Shaping](../../itextshaperfactory/)
* Assemblée [Aspose.Words](../../../)


