---
title: PageSetup.BottomMargin
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Restituisce o imposta la distanza in punti tra il bordo inferiore della pagina e il limite inferiore del corpo del testo.
type: docs
weight: 80
url: /it/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Restituisce o imposta la distanza (in punti) tra il bordo inferiore della pagina e il limite inferiore del corpo del testo.

```csharp
public double BottomMargin { get; set; }
```

### Esempi

Mostra come regolare il formato carta, l'orientamento, i margini e altre impostazioni per una sezione.

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
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


