---
title: "classe Aspose::Words::Saving::HtmlFixedSaveOptions"
linktitle: "HtmlFixedSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Saving::HtmlFixedSaveOptions. Peut être utilisée pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format HtmlFixed. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Peut être utilisée pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [HtmlFixed](../../aspose.words/saveformat/). Pour en savoir plus, consultez l'article de documentation [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Obtient une valeur déterminant la façon dont les couleurs sont rendues. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Spécifie le préfixe qui est ajouté à tous les noms de classe dans le fichier style.css. La valeur par défaut est **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs date/heure. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtient une valeur déterminant comment les effets 3D sont rendus. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les formes DrawingML sont rendues. |
| [get_Encoding](./get_encoding/)() const | Spécifie l'encodage à utiliser lors de l'exportation vers HTML. La valeur par défaut est **new UTF8Encoding(true)** (UTF-8 avec BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Spécifie si le CSS (Cascading [Style](../../aspose.words/style/) Sheet) doit être incorporé dans le document Html. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Spécifie si les polices doivent être incorporées dans le document Html au format Base64. Notez que l'activation de ce drapeau peut augmenter considérablement la taille du fichier Html de sortie. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Spécifie si les images doivent être incorporées dans le document Html au format Base64. Notez que l'activation de ce drapeau peut augmenter considérablement la taille du fichier Html de sortie. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Spécifie si les ressources SVG doivent être incorporées dans le document Html. La valeur par défaut est **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Obtient ou définit l'indication de savoir si les champs de formulaire sont exportés en tant qu'éléments interactifs (comme la balise 'input') plutôt que convertis en texte ou graphiques. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**. |
| [get_FontFormat](./get_fontformat/)() const | Obtient ou définit le [ExportFontFormat](../exportfontformat/) utilisé pour l'exportation des polices. La valeur par défaut est [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Spécifie un préfixe qui est ajouté au début de tous les ID d'éléments générés dans le document de sortie. La valeur par défaut est null et aucun préfixe n'est ajouté. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtient la valeur déterminant si l’optimisation de la mémoire doit être effectuée avant d’enregistrer le document. La valeur par défaut pour cette propriété est **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Permet de spécifier les options de rendu des métafichiers. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Obtient le [NumeralFormat](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Le drapeau indique s'il est nécessaire d'optimiser la sortie. Si ce drapeau est activé, les canevas imbriqués redondants et les canevas vides sont supprimés, de même que les glyphes voisins avec la même mise en forme sont concaténés. Note : La précision de l'affichage du contenu peut être affectée si cette propriété est définie sur **true**. La valeur par défaut est **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Spécifie l'alignement horizontal des pages dans un document HTML. La valeur par défaut est [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Spécifie les marges autour des pages dans un document HTML. La valeur des marges est mesurée en points et doit être égale ou supérieure à 0. La valeur par défaut est de 10 points. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format page fixe. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Lorsque **true**, le formatage « pretty » est appliqué à la sortie lorsque c’est possible. La valeur par défaut est **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Appelé lors de l’enregistrement d’un document et accepte les données concernant la progression de l’enregistrement. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Spécifie si le JavaScript sera supprimé des liens. La valeur par défaut est **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Permet de contrôler la façon dont les ressources (images, polices et css) sont enregistrées lorsqu'un document est exporté au format Html à page fixe. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Spécifie le dossier physique où les ressources (images, polices, css) sont enregistrées lors de l'exportation d'un document au format Html. La valeur par défaut est **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Spécifie le nom du dossier utilisé pour construire les URI d'images écrites dans un document Html. La valeur par défaut est **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Le drapeau indique si les règles CSS \"@font-face\" doivent être placées dans un fichier séparé \"fontFaces.css\" lorsqu'un document est enregistré avec une feuille de style externe (c'est‑à‑dire lorsque [ExportEmbeddedCss](./get_exportembeddedcss/) est **false**). La valeur par défaut est **false**, toutes les règles CSS sont écrites dans un seul fichier \"styles.css\". |
| [get_SaveFormat](./get_saveformat/)() override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Spécifie si la bordure autour des pages doit être affichée. La valeur par défaut est **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement en fichier DOC ou DOCX. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) est mise à jour avant l'enregistrement. La valeur par défaut est **false** ; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtient une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut pour cette propriété est **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) est mise à jour avant l'enregistrement. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) est mise à jour avant l'enregistrement. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtient une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage lors du rendu. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c’est‑à‑dire lents). |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Le drapeau indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si ce drapeau est défini sur **true**, les propriétés [FontFormat](./get_fontformat/) et [ExportEmbeddedFonts](./get_exportembeddedfonts/) n'ont aucun effet, de même que le [ResourceSavingCallback](./get_resourcesavingcallback/) n'est pas déclenché pour les polices. La valeur par défaut est **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Définit une valeur déterminant comment les couleurs sont rendues. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | Spécifie le préfixe qui est ajouté à tous les noms de classe dans le fichier style.css. La valeur par défaut est **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Définit une valeur déterminant comment les effets 3D sont rendus. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Mutateur pour [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Mutateur pour [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Mutateur pour [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Permet de spécifier les options de rendu des métafichiers. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Définit [NumeralFormat](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format page fixe. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Mutateur pour [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Permet de contrôler la façon dont les ressources (images, polices et css) sont enregistrées lorsqu'un document est exporté au format Html à page fixe. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Spécifie si la bordure autour des pages doit être affichée. La valeur par défaut est **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Définit une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Définisseur de [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## Voir aussi

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
