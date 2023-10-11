---
title: PageSetup.Gutter
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Obtient ou définit la quantité despace supplémentaire ajoutée à la marge pour la reliure du document.
type: docs
weight: 160
url: /fr/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Obtient ou définit la quantité d'espace supplémentaire ajoutée à la marge pour la reliure du document.

```csharp
public double Gutter { get; set; }
```

### Exemples

Montre comment configurer un document pouvant être imprimé sous forme de pli de livre.

```csharp
Document doc = new Document();

// Insère un texte qui s'étend sur 16 pages.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propriété "PageSetup" de la première section pour imprimer le document sous la forme d'un pli de livre.
// Lorsqu'on imprime ce document recto verso, on peut prendre les pages pour les empiler
// et pliez-les tous au milieu en même temps. Le contenu du document s’alignera dans un pli de livre.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// On ne peut préciser le nombre de feuilles qu'en multiples de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

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
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


