---
title: PageSetup.BottomMargin
linktitle: BottomMargin
articleTitle: BottomMargin
second_title: Aspose.Words per .NET
description: Regola il layout del documento con la proprietà BottomMargin di PageSetup, definendo lo spazio tra il bordo inferiore della pagina e il corpo del testo per una presentazione ottimale.
type: docs
weight: 80
url: /it/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Restituisce o imposta la distanza (in punti) tra il bordo inferiore della pagina e il limite inferiore del corpo del testo.

```csharp
public double BottomMargin { get; set; }
```

## Esempi

Mostra come regolare il formato della carta, l'orientamento, i margini e altre impostazioni per una sezione.

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

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
