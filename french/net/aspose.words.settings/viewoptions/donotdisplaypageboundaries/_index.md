---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ViewOptions DoNotDisplayPageBoundaries améliore votre mise en page en éliminant l'espace de marge supérieure pour un aspect plus propre et plus professionnel.
type: docs
weight: 20
url: /fr/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Désactive l'affichage de l'espace entre le haut du texte et le bord supérieur de la page.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## Exemples

Montre comment masquer les espaces blancs verticaux et les en-têtes/pieds de page dans les options d'affichage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer du contenu qui s'étend sur 3 pages.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Insérer un en-tête et un pied de page.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Ce document contient une petite quantité de contenu qui occupe quelques pages entières.
// Définissez l'indicateur « DoNotDisplayPageBoundaries » sur « true » pour que les anciennes versions de Microsoft Word omettent les en-têtes,
// pieds de page et une grande partie de l'espace blanc vertical lors de l'affichage de notre document.
// Définissez l'indicateur « DoNotDisplayPageBoundaries » sur « false » pour obtenir les anciennes versions de Microsoft Word
// pour afficher normalement notre document.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Voir également

* class [ViewOptions](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
