---
title: "Classe Aspose::Words::Loading::PdfLoadOptions"
linktitle: "PdfLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Loading::PdfLoadOptions. Consente di specificare opzioni aggiuntive durante il caricamento di un documento Pdf in un oggetto Document. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class


Consente di specificare opzioni aggiuntive durante il caricamento di un documento Pdf in un oggetto [Document](../../aspose.words/document/). Per saperne di più, visita l'articolo di documentazione [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class PdfLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere **null** o una stringa vuota. Il valore predefinito è **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Ottiene o imposta se convertire le immagini metafile ([Wmf](../) o [Emf](../)) nel formato immagine [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office [Math](../../aspose.words.math/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere **null**. Il valore predefinito è **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Consente di specificare le impostazioni del carattere del documento. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Specifica se ignorare i dati OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Ottiene le preferenze linguistiche che verranno utilizzate durante il caricamento del documento. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Specifica il formato del documento da caricare. Il valore predefinito è [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito è [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_PageCount](./get_pagecount/)() const | Restituisce il numero di pagine da leggere. Il valore predefinito è MaxValue, il che significa che verranno lette tutte le pagine del documento. |
| [get_PageIndex](./get_pageindex/)() const | Restituisce l'indice basato su zero della prima pagina da leggere. Il valore predefinito è 0. |
| [get_Password](../loadoptions/get_password/)() const | Ottiene o imposta la password per aprire un documento crittografato. Può essere **null** o una stringa vuota. Il valore predefinito è **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Ottiene o imposta se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Usa questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [get_SkipPdfImages](./get_skippdfimages/)() const | Restituisce il flag che indica se le immagini devono essere ignorate durante il caricamento del documento PDF. Il valore predefinito è **false**. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Specifica se aggiornare i campi con l'attributo **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Ottiene o imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione della pagina. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare la perdita di fedeltà dei dati o della formattazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Inizializza una nuova istanza di questa classe con i valori predefiniti. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate ai valori specificati. |
| [PdfLoadOptions](./pdfloadoptions/)() |  |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter per [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter per [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_PageCount](./set_pagecount/)(int32_t) | Imposta il numero di pagine da leggere. Il valore predefinito è MaxValue, il che significa che verranno lette tutte le pagine del documento. |
| [set_PageIndex](./set_pageindex/)(int32_t) | Imposta l'indice basato su zero della prima pagina da leggere. Il valore predefinito è 0. |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [set_SkipPdfImages](./set_skippdfimages/)(bool) | Imposta il flag che indica se le immagini devono essere ignorate durante il caricamento del documento PDF. Il valore predefinito è **false**. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare la perdita di fedeltà dei dati o della formattazione. |
| static [Type](./type/)() |  |
## Vedi anche

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
