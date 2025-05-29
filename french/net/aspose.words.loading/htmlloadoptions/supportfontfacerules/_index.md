---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words pour .NET
description: Découvrez HtmlLoadOptions SupportFontFaceRules et contrôlez facilement le chargement des polices. Améliorez votre site web en activant des polices personnalisées pour un rendu soigné.
type: docs
weight: 60
url: /fr/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Obtient ou définit une valeur indiquant s'il faut prendre en charge les règles @font-face et s'il faut charger les polices déclarées. La valeur par défaut est`FAUX` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Remarques

Si cette option est activée, les polices déclarées dans les règles @font-face sont chargées et intégrées dans les définitions de polices du document résultant (voir[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Cela rend les polices chargées disponibles pour le rendu, mais n'active pas automatiquement l'intégration des polices lors de l'enregistrement. Pour enregistrer le document avec les polices chargées,[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) propriété de la[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) La collection doit être définie sur`vrai` .

Les formats de police pris en charge sont TTF, EOT et WOFF.

Les règles @font-face ne sont pas prises en charge lors du chargement des images SVG.

## Exemples

Montre comment charger les règles « @font-face » déclarées.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
