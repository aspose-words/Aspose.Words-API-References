---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IdPrefix de HtmlFixedSaveOptions pour personnaliser les identifiants d'éléments dans vos documents. Améliorez l'organisation avec des préfixes personnalisés pour un rendu optimal !
type: docs
weight: 100
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

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

Montre comment ajouter un préfixe ajouté à tous les ID d'éléments générés.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
