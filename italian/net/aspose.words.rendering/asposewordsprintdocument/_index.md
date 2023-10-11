---
title: Class AsposeWordsPrintDocument
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Rendering.AsposeWordsPrintDocument classe. Fornisce unimplementazione predefinita per la stampa di aDocument allinterno del framework di stampa .NET.
type: docs
weight: 4530
url: /it/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Fornisce un'implementazione predefinita per la stampa di a[`Document`](../../aspose.words/document/) all'interno del framework di stampa .NET.

Per saperne di più, visita il[Stampa di un documento a livello di codice o utilizzando le finestre di dialogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) articolo di documentazione.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(Document) | Inizializza una nuova istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Ottiene o imposta la modalità di stampa delle pagine non colorate se il dispositivo supporta la stampa a colori. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Ottiene il numero di pagine stampate a colori (cioè conColor impostato su vero). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Legge e memorizza nella cache alcuni campi diPrinterSettings per ridurre i tempi di stampa. |

### Osservazioni

`AsposeWordsPrintDocument` sovrascrivePrintEventArgs) per stampare l'intervallo di pagine specificato inPrinterSettings.

Un singolo documento Word può essere costituito da più sezioni che specificano pagine con dimensioni, orientamento e vassoi carta diversi.`AsposeWordsPrintDocument` sostituisce QueryPageSettingsEventArgs) per selezionare correttamente il formato carta, l'orientamento e l'origine carta quando si stampa un documento Word.

Microsoft Word memorizza i valori specifici della stampante per i vassoi carta in un documento Word e pertanto, stampando solo sullo stesso modello di stampante selezionato quando l'utente ha specificato i vassoi carta comporterà la stampa dai vassoi corretti. Se stampi un documento su una stampante diversa, molto probabilmente verrà utilizzato il vassoio carta predefinito e non i vassoi specificati nel documento.

### Guarda anche

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)


