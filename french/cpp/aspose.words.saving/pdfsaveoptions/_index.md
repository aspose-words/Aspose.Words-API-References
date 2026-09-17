---
title: "Aspose::Words::Saving::PdfSaveOptions classe"
linktitle: "PdfSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions classe. Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format Pdf. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [Pdf](../../aspose.words/saveformat/). Pour en savoir plus, consultez l'article de documentation [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Crée une copie profonde de cet objet. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | Un indicateur spécifiant s'il faut écrire des opérateurs de positionnement de texte supplémentaires ou non. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Obtient ou définit une valeur déterminant comment les pièces jointes sont incorporées au document PDF. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Obtient ou définit une valeur déterminant s'il faut mettre en cache ou non les graphiques placés en arrière-plan du document. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Obtient une valeur déterminant la façon dont les couleurs sont rendues. |
| [get_Compliance](./get_compliance/)() const | Spécifie le niveau de conformité aux normes PDF pour les documents de sortie. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Spécifie s'il faut convertir les références de notes de bas de page/notes de fin dans le texte principal en hyperliens actifs. Lorsqu'on clique, l'hyperlien mène à la note de bas de page/note de fin correspondante. La valeur par défaut est **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Obtient ou définit une valeur déterminant la manière dont les [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) sont exportées vers le fichier PDF. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs date/heure. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Obtient ou définit les détails pour la signature du document PDF de sortie. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | Un indicateur spécifiant si la barre de titre de la fenêtre doit afficher le titre du document provenant de l'entrée Title du dictionnaire d'informations du document. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtient une valeur déterminant comment les effets 3D sont rendus. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les formes DrawingML sont rendues. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Permet de spécifier les options de sous-échantillonnage. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Contrôle la façon dont les polices sont incorporées dans les documents PDF résultants. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Obtient ou définit les détails pour le chiffrement du document PDF de sortie. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Obtient ou définit une valeur déterminant s'il faut exporter ou non la structure du document. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Obtient ou définit une valeur déterminant si les formes flottantes sont exportées en tant que balises en ligne dans la structure du document. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Obtient ou définit une valeur déterminant s'il faut créer ou non une balise "Span" dans la structure du document pour exporter la langue du texte. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Obtient ou définit une valeur déterminant si un graphique de paragraphe doit être marqué comme un artefact. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Spécifie le mode d'incorporation des polices. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Spécifie s'il faut générer des scripts qui émulent le comportement spécifique des champs de formulaire Microsoft Word dans le PDF. La valeur par défaut est **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Détermine comment les signets dans les en-têtes/pieds de page sont exportés. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Spécifie comment l’espace colorimétrique sera sélectionné pour les images du document PDF. |
| [get_ImageCompression](./get_imagecompression/)() const | Spécifie le type de compression à utiliser pour toutes les images du document. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus. |
| [get_InterpolateImages](./get_interpolateimages/)() const | Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque **false** est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place. |
| [get_JpegQuality](./get_jpegquality/)() | Obtient ou définit une valeur déterminant la qualité des images JPEG à l'intérieur du document PDF. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtient la valeur déterminant si l’optimisation de la mémoire doit être effectuée avant d’enregistrer le document. La valeur par défaut pour cette propriété est **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Permet de spécifier les options de rendu des métafichiers. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Obtient le [NumeralFormat](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Obtient ou définit une valeur déterminant si les hyperliens dans le document Pdf de sortie sont forcés de s'ouvrir dans une nouvelle fenêtre (ou onglet) du navigateur. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Le drapeau indique s'il est nécessaire d'optimiser la sortie. Si ce drapeau est activé, les canevas imbriqués redondants et les canevas vides sont supprimés, de même que les glyphes voisins ayant le même formatage sont concaténés. Remarque : la précision de l'affichage du contenu peut être affectée si cette propriété est définie sur **true**. La valeur par défaut est **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Permet de spécifier les options de contour. |
| [get_PageLayout](./get_pagelayout/)() const | Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF. |
| [get_PageMode](./get_pagemode/)() const | Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans un lecteur PDF. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format page fixe. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document. |
| [get_PreblendImages](./get_preblendimages/)() const | Obtient ou définit une valeur déterminant s'il faut ou non pré-mélanger les images transparentes avec une couleur d'arrière-plan noire. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Spécifie s'il faut conserver les champs de formulaire Microsoft Word en tant que champs de formulaire dans le PDF ou les convertir en texte. La valeur par défaut est **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Lorsque **true**, le formatage « pretty » est appliqué à la sortie lorsque c’est possible. La valeur par défaut est **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Appelé lors de l’enregistrement d’un document et accepte les données concernant la progression de l’enregistrement. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Spécifie s'il faut rendre la bordure du champ de formulaire à choix du PDF. |
| [get_SaveFormat](./get_saveformat/)() override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [Pdf](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement en fichier DOC ou DOCX. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_TextCompression](./get_textcompression/)() const | Spécifie le type de compression à utiliser pour tout le contenu textuel du document. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) est mise à jour avant l'enregistrement. La valeur par défaut est **false** ; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtient une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut pour cette propriété est **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) est mise à jour avant l'enregistrement. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) est mise à jour avant l'enregistrement. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtient une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage lors du rendu. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression en livret, si elle est spécifiée via [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Obtient ou définit une valeur déterminant s'il faut ou non remplacer les polices TrueType Arial, Times New Roman, Courier New et Symbol par les polices PDF Type 1 de base. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c’est‑à‑dire lents). |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Spécifie s'il faut utiliser la balise Tag ou la propriété Id du contrôle SDT comme nom du champ de formulaire dans le PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Obtient une valeur déterminant le type de zoom à appliquer lorsqu'un document est ouvert avec un visualiseur PDF. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Obtient une valeur déterminant le facteur de zoom (en pourcentage) pour un document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Pdf](../../aspose.words/saveformat/). |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Définit une valeur déterminant comment les couleurs sont rendues. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Spécifie le niveau de conformité aux normes PDF pour les documents de sortie. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Spécifie s'il faut convertir les références de notes de bas de page/notes de fin dans le texte principal en hyperliens actifs. Lorsqu'on clique, l'hyperlien mène à la note de bas de page/note de fin correspondante. La valeur par défaut est **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Définit une valeur déterminant comment les effets 3D sont rendus. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Permet de spécifier les options de sous-échantillonnage. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Permet de spécifier les options de rendu des métafichiers. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Définit [NumeralFormat](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Mutateur pour [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans un lecteur PDF. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format page fixe. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Mutateur pour [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut être que [Pdf](../../aspose.words/saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Définit une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Définisseur pour [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Définit une valeur déterminant le type de zoom à appliquer lorsqu'un document est ouvert avec un visualiseur PDF. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Définit une valeur déterminant le facteur de zoom (en pourcentage) pour un document. |
| static [Type](./type/)() |  |
## Voir aussi

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
