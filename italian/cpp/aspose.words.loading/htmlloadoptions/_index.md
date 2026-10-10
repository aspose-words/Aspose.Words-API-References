---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::HtmlLoadOptions class. Consente di specificare opzioni aggiuntive durante il caricamento di un documento HTML in un oggetto Document. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


Consente di specificare opzioni aggiuntive durante il caricamento di un documento HTML in un oggetto [Document](../../aspose.words/document/). Per saperne di più, visita l'articolo di documentazione [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Ottiene o imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere **null** o una stringa vuota. Il valore predefinito è **null**. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Ottiene o imposta un valore che specifica come le proprietà degli elementi a livello di blocco vengono importate. Il valore predefinito è [Merge](../blockimportmode/). |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Ottiene o imposta se convertire le immagini metafile ([Wmf](../) o [Emf](../)) nel formato immagine [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Ottiene o imposta se convertire le forme con EquationXML in oggetti Office [Math](../../aspose.words.math/). |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Ottiene o imposta un valore che indica se convertire le immagini SVG caricate nel formato EMF. Il valore predefinito è **false** e, se possibile, le immagini SVG caricate vengono conservate così come sono senza conversione. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Ottiene o imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere **null**. Il valore predefinito è **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Consente di specificare le impostazioni del carattere del documento. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | Ottiene o imposta un valore che indica se ignorare gli elementi HTML <noscript>. Il valore predefinito è **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Specifica se ignorare i dati OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Ottiene le preferenze linguistiche che verranno utilizzate durante il caricamento del documento. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Specifica il formato del documento da caricare. Il valore predefinito è [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. Il valore predefinito è [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Ottiene o imposta la password per aprire un documento crittografato. Può essere **null** o una stringa vuota. Il valore predefinito è **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | Ottiene o imposta il tipo preferito di nodi del documento che rappresenteranno gli elementi <input> e <select> importati. Il valore predefinito è [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Ottiene o imposta se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Usa questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | Ottiene o imposta un valore che indica se supportare le regole @font-face e se caricare i font dichiarati. Il valore predefinito è **false**. |
| [get_SupportVml](./get_supportvml/)() const | Ottiene o imposta un valore che indica se supportare le immagini VML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è **null** e non vengono utilizzati file temporanei. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Specifica se aggiornare i campi con l'attributo **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Ottiene o imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione della pagina. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare la perdita di fedeltà dei dati o della formattazione. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | Il numero di millisecondi da attendere prima che la richiesta web scada. Il valore predefinito è 100000 millisecondi (100 secondi). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | Inizializza una nuova istanza di questa classe con i valori predefiniti. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate ai valori specificati. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Inizializza una nuova istanza di questa classe con i valori predefiniti. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con la password specificata per caricare un documento crittografato. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Una scorciatoia per inizializzare una nuova istanza di questa classe con le proprietà impostate ai valori specificati. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter per [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | Setter per [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter per [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Impostatore per [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Impostatore per [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Impostatore per [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Impostatore per [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | Impostatore per [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Impostatore per [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare la perdita di fedeltà dei dati o della formattazione. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | Il numero di millisecondi da attendere prima che la richiesta web scada. Il valore predefinito è 100000 millisecondi (100 secondi). |
| static [Type](./type/)() |  |

## Esempi



Mostra come supportare i commenti condizionali durante il caricamento di un documento HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Se il valore è true, allora consideriamo il codice VML durante l'analisi del documento caricato.
loadOptions->set_SupportVml(supportVml);

// Questo documento contiene un'immagine JPEG all'interno dei tag "<!--[if gte vml 1]>",
// e un'immagine PNG diversa all'interno dei tag "<![if !vml]>".
// Se impostiamo il flag "SupportVml" su "true", Aspose.Words caricherà il JPEG.
// Se impostiamo questo flag su "false", Aspose.Words caricherà solo il PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Vedi anche

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
