---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words pour .NET
description: HtmlFixedSaveOptions PageMargins propriété. Spécifie les marges autour des pages dun document HTML. La valeur des marges est mesurée en points et doit être égale ou supérieure à 0. La valeur par défaut est de 10 points en C#.
type: docs
weight: 120
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Spécifie les marges autour des pages d'un document HTML. La valeur des marges est mesurée en points et doit être égale ou supérieure à 0. La valeur par défaut est de 10 points.

```csharp
public double PageMargins { get; set; }
```

## Remarques

Cela dépend de la valeur de[`PageHorizontalAlignment`](../pagehorizontalalignment/) propriété:

* Définit les marges de page supérieure, inférieure et gauche si la valeur estLeft .
* Définit les marges supérieure, inférieure et droite de la page si la valeur estRight .
* Définit les marges supérieure et inférieure de la page si la valeur estCenter .

## Exemples

Montre comment ajuster les marges de la page lors de l’enregistrement d’un document au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### Voir également

* class [HtmlFixedSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
