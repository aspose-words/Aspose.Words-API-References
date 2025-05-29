---
title: PageSetup.HeaderDistance
linktitle: HeaderDistance
articleTitle: HeaderDistance
second_title: Aspose.Words pour .NET
description: Ajustez la propriété PageSetup HeaderDistance pour personnaliser l'espacement des en-têtes en points, améliorant ainsi la mise en page de votre document pour une meilleure lisibilité et présentation.
type: docs
weight: 170
url: /fr/net/aspose.words/pagesetup/headerdistance/
---
## PageSetup.HeaderDistance property

Renvoie ou définit la distance (en points) entre l'en-tête et le haut de la page.

```csharp
public double HeaderDistance { get; set; }
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
