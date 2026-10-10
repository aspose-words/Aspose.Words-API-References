---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions class. Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document aux formats Html, Mhtml, Epub, Azw3 ou Mobi. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document aux formats [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) ou [Mobi](../../aspose.words/saveformat/). Pour en savoir plus, consultez l'article de documentation [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Spécifie si les retraits négatifs gauche et droit des paragraphes sont normalisés lors de l'enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Spécifie un préfixe qui est ajouté à tous les noms de classes CSS. La valeur par défaut est une chaîne vide et les noms de classes CSS générés n'ont aucun préfixe commun. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Permet de contrôler comment les styles CSS sont enregistrés lorsqu'un document est enregistré au format HTML, MHTML ou EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Spécifie le chemin et le nom du fichier de feuille de style en cascade [Style](../../aspose.words/style/) (CSS) écrit lorsqu'un document est exporté vers HTML. La valeur par défaut est une chaîne vide. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Spécifie comment les styles CSS (feuille de style en cascade [Style](../../aspose.words/style/)) sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut est [Inline](../cssstylesheettype/) pour HTML/MHTML et [External](../cssstylesheettype/) pour EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs date/heure. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtient une valeur déterminant comment les effets 3D sont rendus. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les formes DrawingML sont rendues. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Permet de contrôler comment les parties du document sont enregistrées lorsqu'un document est enregistré au format HTML ou EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Spécifie comment le document doit être découpé lors de l'enregistrement aux formats [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) ou [Azw3](../../aspose.words/saveformat/). La valeur par défaut est [None](../documentsplitcriteria/) pour HTML et [HeadingParagraph](../documentsplitcriteria/) pour EPUB et AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Spécifie le niveau maximal de titres auquel le document doit être découpé. La valeur par défaut est **%2**. |
| [get_Encoding](./get_encoding/)() const | Spécifie l'encodage à utiliser lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est **new UTF8Encoding(false)** (UTF-8 sans BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Spécifie s'il faut utiliser des URL CID (Content-ID) pour référencer les ressources (images, polices, CSS) incluses dans les documents MHTML. La valeur par défaut est **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Spécifie s'il faut exporter les propriétés de document intégrées et personnalisées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Contrôle comment les champs de formulaire déroulants sont enregistrés en HTML ou MHTML. La valeur par défaut est **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Spécifie si les ressources de police doivent être exportées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Spécifie si les ressources de polices doivent être incorporées dans le HTML en encodage Base64. La valeur par défaut est **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Spécifie comment les en-têtes et pieds de page sont générés en HTML, MHTML ou EPUB. La valeur par défaut est [PerSection](../exportheadersfootersmode/) pour HTML/MHTML et [None](../exportheadersfootersmode/) pour EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Spécifie si les images sont enregistrées au format Base64 dans le HTML, MHTML ou EPUB de sortie. La valeur par défaut est **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Spécifie si les informations de langue sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Contrôle comment les libellés de listes sont générés en HTML, MHTML ou EPUB. La valeur par défaut est [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Spécifie si l'URL d'origine doit être utilisée comme URL des images liées. La valeur par défaut est **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Spécifie si les marges de page sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Spécifie si la configuration de page est exportée vers HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Spécifie si les tailles de police doivent être émises en unités relatives lors de l’enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Spécifie s’il faut écrire les informations de round‑trip lors de l’enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **true** pour HTML et **false** pour MHTML et EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Contrôle si les nœuds [Shape](../../aspose.words.drawing/shape/) sont convertis en images SVG lors de l’enregistrement en HTML, MHTML, EPUB ou AZW3. La valeur par défaut est **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Contrôle la façon dont les champs de formulaire de saisie de texte sont enregistrés en HTML ou MHTML. La valeur par défaut est **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Spécifie s’il faut écrire les numéros de page dans la table des matières lors de l’enregistrement en HTML, MHTML et EPUB. La valeur par défaut est **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Spécifie s’il faut écrire la déclaration DOCTYPE lors de l’enregistrement en HTML ou MHTML. Lorsque **true**, une déclaration DOCTYPE est écrite dans le document avant l’élément racine. La valeur par défaut est **false**. Lors de l’enregistrement en EPUB ou HTML5 ([Html5](../htmlversion/)), la déclaration DOCTYPE est toujours écrite. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Contrôle quelles ressources de police nécessitent un sous‑ensemble lors de l’enregistrement en HTML, MHTML ou EPUB. La valeur par défaut est **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Permet de contrôler la façon dont les polices sont enregistrées lorsqu’un document est sauvegardé en HTML, MHTML ou EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Spécifie le dossier physique où les polices sont enregistrées lors de l’exportation d’un document en HTML. La valeur par défaut est une chaîne vide. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Spécifie le nom du dossier utilisé pour construire les URI de police écrites dans un document HTML. La valeur par défaut est une chaîne vide. |
| [get_HtmlVersion](./get_htmlversion/)() const | Spécifie la version de la norme HTML qui doit être utilisée lors de l’enregistrement du document en HTML ou MHTML. La valeur par défaut est [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Spécifie la résolution de sortie pour les images lors de l’exportation en HTML, MHTML ou EPUB. La valeur par défaut est **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Permet de contrôler la façon dont les images sont enregistrées lorsqu’un document est sauvegardé en HTML, MHTML ou EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Spécifie le dossier physique où les images sont enregistrées lors de l’exportation d’un document au format HTML. La valeur par défaut est une chaîne vide. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Spécifie le nom du dossier utilisé pour construire les URI d’image écrites dans un document HTML. La valeur par défaut est une chaîne vide. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtient la valeur déterminant si l’optimisation de la mémoire doit être effectuée avant d’enregistrer le document. La valeur par défaut pour cette propriété est **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Spécifie sous quel format les métafichiers sont enregistrés lors de l’exportation en HTML, MHTML ou EPUB. La valeur par défaut est [Png](../htmlmetafileformat/), ce qui signifie que les métafichiers sont rendus en images PNG raster. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Spécifie le niveau maximal de titres remplis dans la carte de navigation lors de l’exportation aux formats EPUB, MOBI ou AZW3. La valeur par défaut est **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Contrôle la façon dont les objets OfficeMath sont exportés en HTML, MHTML ou EPUB. La valeur par défaut est [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Lorsque **true**, le formatage « pretty » est appliqué à la sortie lorsque c’est possible. La valeur par défaut est **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Appelé lors de l’enregistrement d’un document et accepte les données concernant la progression de l’enregistrement. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Spécifie si le JavaScript sera supprimé des liens. La valeur par défaut est **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Spécifie si les caractères antislash doivent être remplacés par des signes yen. La valeur par défaut est **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Spécifie si les noms de familles de polices utilisés dans le document sont résolus et substitués selon [FontSettings](../../aspose.words/document/get_fontsettings/) lors de l'écriture dans des formats basés sur HTML. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Spécifie un dossier physique où toutes les ressources telles que les images, les polices et les CSS externes sont enregistrées lorsqu'un document est exporté vers HTML. La valeur par défaut est une chaîne vide. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Spécifie le nom du dossier utilisé pour construire les URI de toutes les ressources écrites dans un document HTML. La valeur par défaut est une chaîne vide. |
| [get_SaveFormat](./get_saveformat/)() override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut être [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) ou [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Spécifie si les images sont redimensionnées par Aspose.Words à la taille de la forme englobante lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Contrôle la façon dont les largeurs des tables, des lignes et des cellules sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est [All](../htmlelementsizeoutputmode/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement en fichier DOC ou DOCX. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) est mise à jour avant l'enregistrement. La valeur par défaut est **false** ; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtient une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut pour cette propriété est **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) est mise à jour avant l'enregistrement. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) est mise à jour avant l'enregistrement. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtient une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage lors du rendu. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c’est‑à‑dire lents). |
| [GetType](./gettype/)() const override |  |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Html](../../aspose.words/saveformat/). |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document aux formats [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) ou [Mobi](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Mutateur pour [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Permet de contrôler comment les styles CSS sont enregistrés lorsqu'un document est enregistré au format HTML, MHTML ou EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Mutateur pour [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Définit une valeur déterminant comment les effets 3D sont rendus. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Permet de contrôler comment les parties du document sont enregistrées lorsqu'un document est enregistré au format HTML ou EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Permet de contrôler la façon dont les polices sont enregistrées lorsqu’un document est sauvegardé en HTML, MHTML ou EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Permet de contrôler la façon dont les images sont enregistrées lorsqu’un document est sauvegardé en HTML, MHTML ou EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Spécifie si le JavaScript sera supprimé des liens. La valeur par défaut est **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Définisseur de [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Définit une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment utiliser un encodage spécifique lors de l'enregistrement d'un document au format .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier le codage d'un document que nous allons enregistrer.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Par défaut, un document .epub de sortie contiendra tous ses éléments dans une seule partie HTML.
// Un critère de division nous permet de segmenter le document en plusieurs parties HTML.
// Nous définirons les critères pour diviser le document en paragraphes d'en-tête.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire des fichiers HTML de taille supérieure à une taille spécifique.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Spécifiez que nous voulons exporter les propriétés du document.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Montre comment spécifier le dossier pour stocker les images liées après l'enregistrement au format .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Définissez une option pour exporter les champs de formulaire en texte brut au lieu d'éléments d'entrée HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Voir aussi

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
