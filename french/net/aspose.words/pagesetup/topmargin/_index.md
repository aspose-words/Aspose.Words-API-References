---
title: PageSetup.TopMargin
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Renvoie ou définit la distance en points entre le bord supérieur de la page et la limite supérieure du corps du texte.
type: docs
weight: 440
url: /fr/net/aspose.words/pagesetup/topmargin/
---
## PageSetup.TopMargin property

Renvoie ou définit la distance (en points) entre le bord supérieur de la page et la limite supérieure du corps du texte.

```csharp
public double TopMargin { get; set; }
```

### Exemples

Montre comment ajuster le format du papier, l’orientation, les marges, ainsi que d’autres paramètres pour une section.

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
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


