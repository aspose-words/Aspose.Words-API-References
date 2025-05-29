---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words pour .NET
description: Comparez sans effort les documents avec CompareToImages, en enregistrant les différences sous forme d'images pour chaque page, améliorant ainsi la clarté et l'analyse visuelle.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau renvoyé représente une seule page de la sortie rendue sous forme d'image.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | String | Le document original. |
| v2 | String | Le document modifié. |
| imageSaveOptions | ImageSaveOptions | Les options d'enregistrement de l'image de sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau renvoyé représente une seule page de la sortie rendue sous forme d'image.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| v1 | Stream | Le document original. |
| v2 | Stream | Le document modifié. |
| imageSaveOptions | ImageSaveOptions | Les options d'enregistrement de l'image de sortie. |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | CompareOptions | Options de comparaison de documents. |

## Exemples

Montre comment comparer des documents et enregistrer les résultats sous forme d'images.

```csharp
// Il existe plusieurs façons de comparer des documents :
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
