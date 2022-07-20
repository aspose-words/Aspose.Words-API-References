---
title: RightMargin
second_title: Aspose.Words per .NET API Reference
description: Restituisce o imposta la distanza in punti tra il bordo destro della pagina e il limite destro del corpo del testo.
type: docs
weight: 360
url: /it/net/aspose.words/pagesetup/rightmargin/
---
## PageSetup.RightMargin property

Restituisce o imposta la distanza (in punti) tra il bordo destro della pagina e il limite destro del corpo del testo.

```csharp
public double RightMargin { get; set; }
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

* class [PageSetup](../../pagesetup)
* spazio dei nomi [Aspose.Words](../../pagesetup)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->