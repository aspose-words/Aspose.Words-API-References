---
title: "Aspose::Words::Saving::SaveOptions classe"
linktitle: "SaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions classe. Il s'agit d'une classe de base abstraite pour les classes qui permettent à l'utilisateur de spécifier des options supplémentaires lors de l'enregistrement d'un document dans un format particulier. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words.saving/saveoptions/
---
## SaveOptions class


Il s'agit d'une classe de base abstraite pour les classes qui permettent à l'utilisateur de spécifier des options supplémentaires lors de l'enregistrement d'un document dans un format particulier. Pour en savoir plus, consultez l'article de documentation [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class SaveOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [CreateSaveOptions](./createsaveoptions/)(Aspose::Words::SaveFormat) | Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié. |
| static [CreateSaveOptions](./createsaveoptions/)(const System::String\&) | Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni. |
| [get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**. |
| [get_CustomTimeZoneInfo](./get_customtimezoneinfo/)() const | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs date/heure. |
| [get_DefaultTemplate](./get_defaulttemplate/)() const | Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**. |
| [get_Dml3DEffectsRenderingMode](./get_dml3deffectsrenderingmode/)() const | Obtient une valeur déterminant comment les effets 3D sont rendus. |
| virtual [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [get_DmlRenderingMode](./get_dmlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les formes DrawingML sont rendues. |
| [get_ExportGeneratorName](./get_exportgeneratorname/)() const | Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**. |
| [get_ImlRenderingMode](./get_imlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus. |
| [get_MemoryOptimization](./get_memoryoptimization/)() const | Obtient la valeur déterminant si l’optimisation de la mémoire doit être effectuée avant d’enregistrer le document. La valeur par défaut pour cette propriété est **false**. |
| [get_PrettyFormat](./get_prettyformat/)() const | Lorsque **true**, le formatage « pretty » est appliqué à la sortie lorsque c’est possible. La valeur par défaut est **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Appelé lors de l’enregistrement d’un document et accepte les données concernant la progression de l’enregistrement. |
| virtual [get_SaveFormat](./get_saveformat/)() | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. |
| [get_TempFolder](./get_tempfolder/)() const | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement en fichier DOC ou DOCX. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/)() const | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) est mise à jour avant l'enregistrement. La valeur par défaut est **false** ; |
| [get_UpdateFields](./get_updatefields/)() const | Obtient une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut pour cette propriété est **true**. |
| [get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) est mise à jour avant l'enregistrement. |
| [get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) est mise à jour avant l'enregistrement. |
| [get_UpdateOleControlImages](./get_updateolecontrolimages/)() const | Obtient une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [get_UseAntiAliasing](./get_useantialiasing/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage lors du rendu. |
| [get_UseHighQualityRendering](./get_usehighqualityrendering/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c’est‑à‑dire lents). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](./set_allowembeddingpostscriptfonts/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](./set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](./get_customtimezoneinfo/). |
| [set_DefaultTemplate](./set_defaulttemplate/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](./get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](./set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Définit une valeur déterminant comment les effets 3D sont rendus. |
| virtual [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](./set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](./get_dmlrenderingmode/). |
| [set_ExportGeneratorName](./set_exportgeneratorname/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](./get_exportgeneratorname/). |
| [set_ImlRenderingMode](./set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](./get_imlrenderingmode/). |
| [set_MemoryOptimization](./set_memoryoptimization/)(bool) | Définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **false**. |
| [set_PrettyFormat](./set_prettyformat/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](./get_prettyformat/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](./get_progresscallback/). |
| virtual [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](./set_updateambiguoustextfont/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](./set_updatecreatedtimeproperty/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/). |
| [set_UpdateFields](./set_updatefields/)(bool) | Définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **true**. |
| [set_UpdateLastPrintedProperty](./set_updatelastprintedproperty/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](./set_updatelastsavedtimeproperty/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](./set_updateolecontrolimages/)(bool) | Définit une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [set_UseAntiAliasing](./set_useantialiasing/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](./get_useantialiasing/). |
| [set_UseHighQualityRendering](./set_usehighqualityrendering/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](./get_usehighqualityrendering/). |
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

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
