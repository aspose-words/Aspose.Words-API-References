---
title: PageSetup.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Orientation de la mise en page pour ajuster facilement la mise en page de votre document. Optimisez vos impressions grâce à des paramètres d'orientation personnalisables !
type: docs
weight: 290
url: /fr/net/aspose.words/pagesetup/orientation/
---
## PageSetup.Orientation property

Renvoie ou définit l'orientation de la page.

```csharp
public Orientation Orientation { get; set; }
```

## Remarques

Changement`Orientation` échanges[`PageWidth`](../pagewidth/) et[`PageHeight`](../pageheight/).

## Exemples

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifiez les propriétés de configuration de la page pour la section actuelle du générateur et ajoutez du texte.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si nous commençons une nouvelle section en utilisant un générateur de documents,
// il héritera des propriétés de configuration de page actuelles du constructeur.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Nous pouvons rétablir ses propriétés de configuration de page à leurs valeurs par défaut en utilisant la méthode « ClearFormatting ».
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Voir également

* enum [Orientation](../../orientation/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
