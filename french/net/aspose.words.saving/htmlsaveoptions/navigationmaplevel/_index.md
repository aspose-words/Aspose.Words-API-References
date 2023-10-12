---
title: HtmlSaveOptions.NavigationMapLevel
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Spécifie le niveau maximum de titres renseignés sur la carte de navigation lors de lexportation aux formats EPUB MOBI ou AZW3 . La valeur par défaut est3 .
type: docs
weight: 390
url: /fr/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Spécifie le niveau maximum de titres renseignés sur la carte de navigation lors de l'exportation aux formats EPUB, MOBI ou AZW3 . La valeur par défaut est`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

### Remarques

La carte de navigation permet aux agents utilisateurs de fournir un moyen simple de navigation dans la structure du document. Habituellement, les points de navigation correspondent aux titres du document. Afin de renseigner les rubriques jusqu'au niveau **N** attribuer cette valeur à`NavigationMapLevel`.

Par défaut, trois niveaux de titres sont renseignés : paragraphes de styles **Titre 1** , **Titre 2** et **Titre 3**. Vous pouvez définir cette propriété sur une valeur de 1 à 9 afin de demander le niveau maximum correspondant. La définir sur zéro réduira la carte de navigation à la ou aux racines du document uniquement.

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


