---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.PdfPageLayout per una visualizzazione ottimale dei PDF. Personalizza i layout di pagina per una migliore leggibilità in qualsiasi lettore PDF.
type: docs
weight: 6290
url: /it/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Specifica il layout di pagina da utilizzare quando il documento viene aperto in un lettore PDF.

```csharp
public enum PdfPageLayout
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| SinglePage | `0` | Visualizza una pagina alla volta. |
| OneColumn | `1` | Visualizza le pagine in una colonna. |
| TwoColumnLeft | `2` | Visualizza le pagine su due colonne, con le pagine dispari a sinistra. |
| TwoColumnRight | `3` | Visualizza le pagine su due colonne, con le pagine dispari a destra. |
| TwoPageLeft | `4` | Visualizza le pagine due alla volta, con le pagine dispari a sinistra. |
| TwoPageRight | `5` | Visualizza le pagine due alla volta, con le pagine dispari a destra. |

## Esempi

Mostra come visualizzare le pagine quando vengono aperte in un lettore PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Visualizza le pagine due alla volta, con le pagine dispari a sinistra.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
