---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SvgSaveOptions IdPrefix, qui personnalise les identifiants des éléments dans votre document de sortie pour une meilleure organisation et clarté. Améliorez vos fichiers SVG dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

Spécifie un préfixe qui est ajouté au début de tous les ID d'éléments générés dans le document de sortie. La valeur par défaut est nulle et aucun préfixe n'est ajouté au début.

```csharp
public string IdPrefix { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | La valeur ne répond pas aux exigences spécifiées ci-dessus. |

## Remarques

Si le préfixe est spécifié, il ne peut contenir que des lettres, des chiffres, des traits de soulignement et des tirets, et doit commencer par une lettre.

## Exemples

Montre comment ajouter un préfixe ajouté à tous les ID d'éléments générés (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Voir également

* class [SvgSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
