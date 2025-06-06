---
title: PageSetup.LeftMargin
linktitle: LeftMargin
articleTitle: LeftMargin
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup LeftMargin pour ajuster facilement la marge gauche en points, améliorant ainsi la mise en page et la lisibilité de votre document.
type: docs
weight: 200
url: /fr/net/aspose.words/pagesetup/leftmargin/
---
## PageSetup.LeftMargin property

Renvoie ou définit la distance (en points) entre le bord gauche de la page et la limite gauche du corps du texte.

```csharp
public double LeftMargin { get; set; }
```

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

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
