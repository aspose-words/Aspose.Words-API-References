---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup OddAndEvenPagesHeaderFooter pour des en-têtes et des pieds de page uniques sur les pages paires et impaires, améliorant ainsi la présentation de votre document.
type: docs
weight: 280
url: /fr/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Vrai si le document a des en-têtes et des pieds de page différents pour les pages paires et impaires.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Remarques

Remarque : la modification de cette propriété affecte toutes les sections du document.

## Exemples

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez que nous voulons des en-têtes et des pieds de page différents pour les premières pages, les pages paires et les pages impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Créez les en-têtes, puis ajoutez trois pages au document pour afficher chaque type d'en-tête.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Montre comment activer ou désactiver même les en-têtes/pieds de page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'en-têtes/pieds de page.
// 1 - L'en-tête/pied de page « Principal », qui apparaît sur chaque page de la section.
// Nous pouvons remplacer l'en-tête/pied de page principal par un en-tête/pied de page de première page et un en-tête/pied de page pair.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - L'en-tête/pied de page « Pair », qui apparaît sur chaque page paire de cette section.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Chaque section possède un objet « PageSetup » qui spécifie les propriétés liées à l'apparence de la page
// tels que l'orientation, la taille et les bordures.
// Définissez la propriété « OddAndEvenPagesHeaderFooter » sur « true »
// pour afficher l'en-tête/pied de page pair sur les pages paires.
// Définissez la propriété « OddAndEvenPagesHeaderFooter » sur « false »
// pour afficher l'en-tête/pied de page principal sur les pages paires.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
