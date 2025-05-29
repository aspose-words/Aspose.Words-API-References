---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SavePictureBullet de DocSaveOptions optimise la sortie de vos documents. Contrôlez facilement l'enregistrement des données PictureBullet pour des résultats optimaux.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Quand`FAUX` Les données PictureBullet ne sont pas enregistrées dans le document de sortie. La valeur par défaut est`vrai` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Remarques

Cette option est fournie pour Word 97, qui ne peut pas fonctionner correctement avec les données PictureBullet. Pour supprimer les données PictureBullet, définissez l'option sur « false ».

## Exemples

Montre comment omettre les données PictureBullet du document lors de l'enregistrement.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Certains traitements de texte, tels que Microsoft Word 97, sont incompatibles avec les données PictureBullet.
// En définissant un indicateur dans l'objet SaveOptions,
// nous pouvons convertir toutes les puces d'image en puces ordinaires lors de l'enregistrement.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Voir également

* class [DocSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
