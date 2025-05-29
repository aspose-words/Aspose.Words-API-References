---
title: ChmLoadOptions Class
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Loading.ChmLoadOptions per un caricamento migliorato dei documenti CHM. Personalizza il tuo oggetto Documento con opzioni flessibili per risultati ottimali.
type: docs
weight: 4020
url: /it/net/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamento di un documento CHM in un[`Document`](../../aspose.words/document/) oggetto.

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public class ChmLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ChmLoadOptions](chmloadoptions/)() | Inizializza una nuova istanza di questa classe con valori predefiniti. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire metafile(Wmf OEmf ) immagini aPngformato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`null` Il valore predefinito è`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Consente di specificare le impostazioni del font del documento. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifica se ignorare i dati OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze di lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito èWord2019 |
| [OriginalFileName](../../aspose.words.loading/chmloadoptions/originalfilename/) { get; set; } | Il nome del file CHM. Il valore predefinito è`null` . |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ottiene o imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Viene chiamato durante il caricamento di un documento e accetta dati sullo stato di avanzamento del caricamento. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Consente di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ottiene o imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti di impostazione della pagina. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |

## Esempi

Mostra come risolvere URL come "ms-its:myfile.chm::/index.htm".

```csharp
// Il nostro documento contiene URL come "ms-its:amhelp.chm::....htm", ma ha un nome diverso,
// quindi i collegamenti ai file non funzionano dopo averli salvati in HTML.
// Per evitare questo comportamento, dobbiamo definire il nome del file originale in 'ChmLoadOptions'.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Guarda anche

* class [LoadOptions](../loadoptions/)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
