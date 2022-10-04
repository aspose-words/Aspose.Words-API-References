---
title: PdfLoadOptions
second_title: Aspose.Words per .NET API Reference
description: Consente di specificare opzioni aggiuntive durante il caricamento di un documento Pdf in un fileDocument../aspose.words/document/ oggetto.
type: docs
weight: 3470
url: /it/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

Consente di specificare opzioni aggiuntive durante il caricamento di un documento Pdf in un file[`Document`](../../aspose.words/document/) oggetto.

```csharp
public class PdfLoadOptions : LoadOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PdfLoadOptions](pdfloadoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando richiesto. Può essere una stringa nulla o vuota. Il valore predefinito è null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ottiene o imposta se convertire il metafile (Wmf oEmf ) immagini aPng formato immagine. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ottiene o imposta se convertire forme con EquationXML in oggetti Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere nullo. Il valore predefinito è null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Consente di specificare le impostazioni del carattere del documento. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ottiene le preferenze della lingua che verranno utilizzate durante il caricamento del documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifica il formato del documento da caricare. Il valore predefinito èAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Consente di specificare che il processo di caricamento del documento deve corrispondere a una specifica versione di MS Word. Il valore predefinito èWord2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Ottiene o imposta il numero di pagine da leggere. Il valore predefinito è MaxValue, il che significa che tutte le pagine del documento verranno lette. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Ottiene o imposta l'indice in base 0 della prima pagina da leggere. Il valore predefinito è 0. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ottiene o imposta la password per l'apertura di un documento crittografato. Può essere una stringa nulla o vuota. Il valore predefinito è null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ottiene o imposta se mantenere il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Chiamato durante il caricamento di un documento e accetta i dati sull'avanzamento del caricamento. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Consente di controllare come vengono caricate le risorse esterne (immagini, fogli di stile) quando un documento viene importato da HTML, MHTML. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | Ottiene o imposta il flag che indica se le immagini devono essere saltate durante il caricamento del documento PDF. L'impostazione predefinita è False. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifica se aggiornare i campi con il`sporco` attributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione. |

### Guarda anche

* class [LoadOptions](../loadoptions/)
* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
