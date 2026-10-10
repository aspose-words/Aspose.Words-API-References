---
title: "Aspose::Words::Saving::MarkdownSaveOptions class"
linktitle: "MarkdownSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions class. Classe permettant de spécifier des options supplémentaires lors de l'enregistrement d'un document au format Markdown. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class


Classe permettant de spécifier des options supplémentaires lors de l'enregistrement d'un document au format [Markdown](../../aspose.words/saveformat/). Pour en savoir plus, consultez l'article de documentation [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class MarkdownSaveOptions : public Aspose::Words::Saving::TxtSaveOptionsBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs date/heure. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtient une valeur déterminant comment les effets 3D sont rendus. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les formes DrawingML sont rendues. |
| [get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/)() const | Spécifie comment exporter les paragraphes vides vers Markdown. La valeur par défaut est [EmptyLine](../markdownemptyparagraphexportmode/). |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | Spécifie l'encodage à utiliser lors de l'exportation dans des formats texte. La valeur par défaut est **Encoding.UTF8**. |
| [get_ExportAsHtml](./get_exportashtml/)() const | Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut. La valeur par défaut est [None](../markdownexportashtml/). |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**. |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | Spécifie la manière dont les en-têtes et pieds de page sont exportés vers les formats texte. La valeur par défaut est [PrimaryOnly](../txtexportheadersfootersmode/). |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est **false**. |
| [get_ExportUnderlineFormatting](./get_exportunderlineformatting/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut exporter le format de texte souligné sous forme d'une séquence de deux caractères plus "++". La valeur par défaut est **false**. |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | Permet de spécifier si les sauts de page doivent être conservés lors de l'exportation. La valeur par défaut est **false**. |
| [get_ImageResolution](./get_imageresolution/)() const | Spécifie la résolution de sortie pour les images lors de l'exportation vers Markdown. La valeur par défaut est **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Permet de contrôler la façon dont les images sont enregistrées lorsqu'un document est enregistré au format [Markdown](../../aspose.words/saveformat/). |
| [get_ImagesFolder](./get_imagesfolder/)() const | Spécifie le dossier physique où les images sont enregistrées lors de l'exportation d'un document au format [Markdown](../../aspose.words/saveformat/). La valeur par défaut est une chaîne vide. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Spécifie le nom du dossier utilisé pour construire les URI d'images écrites dans un document. La valeur par défaut est une chaîne vide. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus. |
| [get_LinkExportMode](./get_linkexportmode/)() const | Spécifie comment les liens seront écrits dans le fichier de sortie. La valeur par défaut est [Auto](../markdownlinkexportmode/). |
| [get_ListExportMode](./get_listexportmode/)() const | Spécifie comment les éléments de liste seront écrits dans le fichier de sortie. La valeur par défaut est [MarkdownSyntax](../markdownlistexportmode/). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtient la valeur déterminant si l’optimisation de la mémoire doit être effectuée avant d’enregistrer le document. La valeur par défaut pour cette propriété est **false**. |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut est [Text](../markdownofficemathexportmode/). |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation dans des formats texte. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Lorsque **true**, le formatage « pretty » est appliqué à la sortie lorsque c’est possible. La valeur par défaut est **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Appelé lors de l’enregistrement d’un document et accepte les données concernant la progression de l’enregistrement. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Permet de contrôler la façon dont les ressources sont enregistrées lorsqu'un document est exporté au format [Markdown](../../aspose.words/saveformat/). |
| [get_SaveFormat](./get_saveformat/)() override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [Markdown](../../aspose.words/saveformat/). |
| [get_TableContentAlignment](./get_tablecontentalignment/)() const | Obtient ou définit une valeur qui spécifie comment aligner le contenu des tableaux lors de l'exportation au format [Markdown](../../aspose.words/saveformat/). La valeur par défaut est [Auto](../tablecontentalignment/). |
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
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MarkdownSaveOptions](./markdownsaveoptions/)() | Initialise une nouvelle instance de cette classe pouvant être utilisée pour enregistrer un document au format [Markdown](../../aspose.words/saveformat/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Définit une valeur déterminant comment les effets 3D sont rendus. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_EmptyParagraphExportMode](./set_emptyparagraphexportmode/)(Aspose::Words::Saving::MarkdownEmptyParagraphExportMode) | Définisseur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/). |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Définisseur pour [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](../txtsaveoptionsbase/get_encoding/). |
| [set_ExportAsHtml](./set_exportashtml/)(Aspose::Words::Saving::MarkdownExportAsHtml) | Définisseur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml](./get_exportashtml/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | Définisseur pour [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Définisseur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportUnderlineFormatting](./set_exportunderlineformatting/)(bool) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting](./get_exportunderlineformatting/). |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | Mutateur pour [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Permet de contrôler la façon dont les images sont enregistrées lorsqu'un document est enregistré au format [Markdown](../../aspose.words/saveformat/). |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_LinkExportMode](./set_linkexportmode/)(Aspose::Words::Saving::MarkdownLinkExportMode) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode](./get_linkexportmode/). |
| [set_ListExportMode](./set_listexportmode/)(Aspose::Words::Saving::MarkdownListExportMode) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode](./get_listexportmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **false**. |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::MarkdownOfficeMathExportMode) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode](./get_officemathexportmode/). |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Permet de contrôler la façon dont les ressources sont enregistrées lorsqu'un document est exporté au format [Markdown](../../aspose.words/saveformat/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [Markdown](../../aspose.words/saveformat/). |
| [set_TableContentAlignment](./set_tablecontentalignment/)(Aspose::Words::Saving::TableContentAlignment) | Mutateur pour [Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment](./get_tablecontentalignment/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Définit une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |
## Voir aussi

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
