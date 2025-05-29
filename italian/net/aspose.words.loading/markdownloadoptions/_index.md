---
title: MarkdownLoadOptions Class
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.MarkdownLoadOptions per migliorare l'esperienza di caricamento dei documenti Markdown. Personalizza le opzioni per una perfetta integrazione nei tuoi progetti.
type: docs
weight: 4120
url: /it/net/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamentoMarkdown documento in un[`Document`](../../aspose.words/document/) oggetto.

```csharp
public class MarkdownLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MarkdownLoadOptions](markdownloadoptions/)() | Inizializza una nuova istanza di`MarkdownLoadOptions` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire metafile(Wmf OEmf ) immagini aPngformato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere`null` Il valore predefinito è`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Consente di specificare le impostazioni del font del documento. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifica se ignorare i dati OLE. |
| [ImportUnderlineFormatting](../../aspose.words.loading/markdownloadoptions/importunderlineformatting/) { get; set; } | Ottiene o imposta un valore booleano che indica di riconoscere una sequenza di due caratteri più "++" come formattazione del testo sottolineato. Il valore predefinito è`falso` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze di lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito èWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere`null` o stringa vuota. Il valore predefinito è`null` . |
| [PreserveEmptyLines](../../aspose.words.loading/markdownloadoptions/preserveemptylines/) { get; set; } | Ottiene o imposta un valore booleano che indica se preservare le righe vuote durante il caricamento di unMarkdown document. Il valore predefinito è`falso` . |
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

Mostra come preservare la riga vuota durante il caricamento di un documento.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Guarda anche

* class [LoadOptions](../loadoptions/)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
