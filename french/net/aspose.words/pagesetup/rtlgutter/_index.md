---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words pour .NET
description: PageSetup RtlGutter propriété. Obtient ou définit si Microsoft Word utilise des gouttières pour la section basée sur une langue de droite à gauche ou une langue de gauche à droite en C#.
type: docs
weight: 380
url: /fr/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Obtient ou définit si Microsoft Word utilise des gouttières pour la section basée sur une langue de droite à gauche ou une langue de gauche à droite.

```csharp
public bool RtlGutter { get; set; }
```

## Exemples

Montre comment définir les marges de gouttière.

```csharp
Document doc = new Document();

// Insère du texte qui s'étend sur plusieurs pages.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Une gouttière ajoute des espaces dans la marge gauche ou droite de la page,
// qui compense le pliage central des pages d'un livre empiétant sur la mise en page de la page.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// Déterminez l'espace dont disposent nos pages pour le texte dans les marges, puis ajoutez une quantité pour remplir une marge.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Définissez la propriété "RtlGutter" sur "true" pour placer la gouttière dans une position plus appropriée pour le texte de droite à gauche.
pageSetup.RtlGutter = true;

// Définissez la propriété "MultiplePages" sur "MultiplePagesType.MirrorMargins" pour alterner
// la position côté gauche/droite des marges de chaque page.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
