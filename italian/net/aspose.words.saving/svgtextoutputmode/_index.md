---
title: Enum SvgTextOutputMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.SvgTextOutputMode enum. Permette di specificare come deve essere reso il testo allinterno di un documento durante il salvataggio in formato SVG.
type: docs
weight: 5610
url: /it/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Permette di specificare come deve essere reso il testo all'interno di un documento durante il salvataggio in formato SVG.

```csharp
public enum SvgTextOutputMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseSvgFonts | `0` | I caratteri SVG vengono utilizzati per il rendering del testo. Tieni presente che non tutti i browser supportano i caratteri SVG. |
| UseTargetMachineFonts | `1` | I caratteri installati sul computer di destinazione vengono utilizzati per eseguire il rendering del testo. Nota: se alcuni dei caratteri utilizzati nel documento non sono disponibili sul computer di destinazione, il documento può apparire diversamente. |
| UsePlacedGlyphs | `2` | Il testo viene renderizzato utilizzando le curve. Tieni presente che la selezione del testo non funzionerà se utilizzi questa opzione. |

### Esempi

Mostra come imitare le proprietà delle immagini durante la conversione di un documento .docx in .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configura l'oggetto SvgSaveOptions per il salvataggio senza bordi della pagina o testo selezionabile.
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


