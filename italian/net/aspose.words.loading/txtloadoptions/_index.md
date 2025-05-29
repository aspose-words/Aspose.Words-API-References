---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.TxtLoadOptions per un caricamento migliorato dei documenti di testo. Personalizza il tuo oggetto Documento con opzioni flessibili per prestazioni ottimali.
type: docs
weight: 4190
url: /it/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamentoText documento in un[`Document`](../../aspose.words/document/) oggetto.

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Inizializza una nuova istanza di questa classe con valori predefiniti. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Ottiene o imposta un valore booleano che indica che verrà eseguito il rilevamento automatico della numerazione durante il caricamento di un documento. Il valore predefinito è`VERO` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire metafile(Wmf OEmf ) immagini aPngformato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | Specifica se rilevare i collegamenti ipertestuali nel testo. Il valore predefinito è`falso` . |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Consente di specificare come vengono riconosciuti gli elementi dell'elenco numerato quando il documento viene importato dal formato di testo normale. Il valore predefinito è`VERO`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Ottiene o imposta una direzione del documento. Il valore predefinito èLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`null` Il valore predefinito è`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Consente di specificare le impostazioni del font del documento. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifica se ignorare i dati OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze di lingua che verranno utilizzate durante il caricamento del documento. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Ottiene o imposta l'opzione preferita di una gestione dello spazio iniziale. Il valore predefinito èConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito èWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ottiene o imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Viene chiamato durante il caricamento di un documento e accetta dati sullo stato di avanzamento del caricamento. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Consente di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Ottiene o imposta l'opzione preferita di una gestione dello spazio finale. Il valore predefinito èTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ottiene o imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti di impostazione della pagina. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |

## Esempi

Mostra come leggere e visualizzare i collegamenti ipertestuali.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Carica il documento con i collegamenti ipertestuali.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Stampa il testo dei collegamenti ipertestuali.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Guarda anche

* class [LoadOptions](../loadoptions/)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
