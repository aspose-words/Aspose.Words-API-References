---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Watermark per aggiungere e personalizzare facilmente filigrane nei tuoi documenti, migliorando così la professionalità e il branding.
type: docs
weight: 7520
url: /it/net/aspose.words/watermark/
---
## Watermark class

Rappresenta la classe per lavorare con la filigrana del documento.

Per saperne di più, visita il[Lavorare con la filigrana](https://docs.aspose.com/words/net/working-with-watermark/) articolo di documentazione.

```csharp
public sealed class Watermark
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Ottiene il tipo di filigrana. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Rimuove la filigrana. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Aggiunge la filigrana dell'immagine nel documento. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Aggiunge la filigrana dell'immagine nel documento. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Aggiunge la filigrana dell'immagine nel documento. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Aggiunge la filigrana dell'immagine nel documento. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Aggiunge una filigrana di testo al documento. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Aggiunge una filigrana di testo al documento. |

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
