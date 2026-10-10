---
title: "Classe Aspose::Words::Loading::TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Loading::TxtLoadOptions. Consente di specificare opzioni aggiuntive durante il caricamento di un documento Text in un oggetto Document. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


Consente di specificare opzioni aggiuntive durante il caricamento del documento [Text](../../aspose.words/loadformat/) in un oggetto [Document](../../aspose.words/document/). Per saperne di più, visita l'articolo di documentazione [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Ottiene o imposta un valore booleano che indica se verrà eseguita la rilevazione automatica della numerazione durante il caricamento di un documento. Il valore predefinito è **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere **null** o una stringa vuota. Il valore predefinito è **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Ottiene o imposta se convertire le immagini metafile ([Wmf](../) o [Emf](../)) nel formato immagine [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office [Math](../../aspose.words.math/). |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Specifica se rilevare i collegamenti ipertestuali nel testo. Il valore predefinito è **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Consente di specificare come vengono riconosciuti gli elementi di elenchi numerati quando il documento è importato da formato di testo semplice. Il valore predefinito è **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Ottiene o imposta la direzione del documento. Il valore predefinito è [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere **null**. Il valore predefinito è **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Consente di specificare le impostazioni del carattere del documento. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Specifica se ignorare i dati OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Ottiene le preferenze linguistiche che verranno utilizzate durante il caricamento del documento. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Ottiene o imposta l'opzione preferita per la gestione degli spazi iniziali. Il valore predefinito è [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Specifica il formato del documento da caricare. Il valore predefinito è [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito è [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Ottiene o imposta la password per aprire un documento crittografato. Può essere **null** o una stringa vuota. Il valore predefinito è **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Ottiene o imposta se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Usa questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Ottiene o imposta l'opzione preferita per la gestione degli spazi finali. Il valore predefinito è [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Specifica se aggiornare i campi con l'attributo **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Ottiene o imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione della pagina. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare la perdita di fedeltà dei dati o della formattazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Inizializza una nuova istanza di questa classe con i valori predefiniti. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate ai valori specificati. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Impostatore per [Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection](./get_autonumberingdetection/). |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter per [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter per [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Impostatore per [Aspose::Words::Loading::TxtLoadOptions::get_DetectHyperlinks](./get_detecthyperlinks/). |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Impostatore per [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Impostatore per [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Impostatore per [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Impostatore per [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare la perdita di fedeltà dei dati o della formattazione. |
| [TxtLoadOptions](./txtloadoptions/)() | Inizializza una nuova istanza di questa classe con i valori predefiniti. |
| static [Type](./type/)() |  |

## Esempi



Mostra come leggere e visualizzare i collegamenti ipertestuali.
```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Carica il documento con collegamenti ipertestuali.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Stampa il testo dei collegamenti ipertestuali.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```

## Vedi anche

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
