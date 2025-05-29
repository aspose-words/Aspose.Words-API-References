---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.TextWatermarkOptions per filigrane di testo personalizzabili. Arricchisci i tuoi documenti con opzioni di branding uniche e professionali!
type: docs
weight: 7290
url: /it/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Contiene opzioni che possono essere specificate quando si aggiunge una filigrana con testo.

Per saperne di più, visita il[Lavorare con la filigrana](https://docs.aspose.com/words/net/working-with-watermark/) articolo di documentazione.

```csharp
public class TextWatermarkOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Ottiene o imposta il colore del carattere. Il valore predefinito èSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Ottiene o imposta il nome della famiglia di font. Il valore predefinito è "Calibri". |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Ottiene o imposta una dimensione del carattere. Il valore predefinito è 0 - auto. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Ottiene o imposta un valore booleano responsabile dell'opacità della filigrana. Il valore predefinito è`VERO` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Ottiene o imposta il layout della filigrana. Il valore predefinito èDiagonal . |

## Esempi

Mostra come creare una filigrana di testo.

```csharp
Document doc = new Document();

// Aggiungi una filigrana di testo normale.
doc.Watermark.SetText("Aspose Watermark");

// Se desideriamo modificare la formattazione del testo utilizzandola come filigrana,
// Possiamo farlo passando un oggetto TextWatermarkOptions quando creiamo la filigrana.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Possiamo rimuovere una filigrana da un documento come questo.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
