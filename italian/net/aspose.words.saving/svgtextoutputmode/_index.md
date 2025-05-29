---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.SvgTextOutputMode per personalizzare il rendering del testo in formato SVG, migliorando la presentazione e l'attrattiva visiva del documento.
type: docs
weight: 6410
url: /it/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Consente di specificare come deve essere visualizzato il testo all'interno di un documento quando si salva in formato SVG.

```csharp
public enum SvgTextOutputMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseSvgFonts | `0` | I font SVG vengono utilizzati per il rendering del testo. Nota: non tutti i browser supportano i font SVG. |
| UseTargetMachineFonts | `1` | Per il rendering del testo vengono utilizzati i font installati sul computer di destinazione. Nota: se alcuni dei font utilizzati nel documento non sono disponibili sul computer di destinazione, il documento potrebbe apparire diverso. |
| UsePlacedGlyphs | `2` | Il testo viene renderizzato utilizzando le curve. Nota: la selezione del testo non funzionerà se si utilizza questa opzione. |

## Esempi

Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configurare l'oggetto SvgSaveOptions per salvare senza bordi di pagina o testo selezionabile.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
