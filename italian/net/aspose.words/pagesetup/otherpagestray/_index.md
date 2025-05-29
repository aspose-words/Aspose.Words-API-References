---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageSetup OtherPagesTray per personalizzare facilmente le impostazioni del vassoio carta della tua stampante. Ottimizza l'efficienza di stampa per ogni sezione!
type: docs
weight: 300
url: /it/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Ottiene o imposta il vassoio della carta (cestino) da utilizzare per tutte le pagine di una sezione tranne la prima. Il valore è specifico dell'implementazione (stampante).

```csharp
public int OtherPagesTray { get; set; }
```

## Esempi

Mostra come far sì che tutte le sezioni di un documento utilizzino il vassoio carta predefinito della stampante selezionata.

```csharp
Document doc = new Document();

// Troviamo la stampante predefinita che utilizzeremo per stampare questo documento.
// È possibile definire una stampante specifica utilizzando la proprietà "PrinterName" dell'oggetto PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Il valore del vassoio carta memorizzato nei documenti è specifico della stampante.
// Ciò significa che il codice seguente reimposta tutti i valori del vassoio pagina per utilizzare il vassoio predefinito della stampante corrente.
// È possibile enumerare PrinterSettings.PaperSources per trovare gli altri valori validi del vassoio carta della stampante selezionata.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Mostra come impostare la stampa utilizzando vassoi di stampa diversi per formati di carta diversi.

```csharp
Document doc = new Document();

// Troviamo la stampante predefinita che utilizzeremo per stampare questo documento.
// È possibile definire una stampante specifica utilizzando la proprietà "PrinterName" dell'oggetto PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Questo è il vassoio che utilizzeremo per le pagine in formato carta "A4".
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Questo è il vassoio che utilizzeremo per le pagine in formato carta "Lettera".
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Modificare l'oggetto PageSettings di questa sezione per far sì che Microsoft Word invii istruzioni alla stampante
// per utilizzare uno dei vassoi identificati sopra, a seconda del formato della carta di questa sezione.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
