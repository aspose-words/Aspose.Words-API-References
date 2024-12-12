---
title: Aspose::Words::Saving::SaveOptions class
linktitle: SaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SaveOptions class. This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format. To learn more, visit the  documentation article in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words.saving/saveoptions/
---
## SaveOptions class


This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class SaveOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| static [CreateSaveOptions](./createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](./createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_CustomTimeZoneInfo](./get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](./get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_Dml3DEffectsRenderingMode](./get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](./get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportGeneratorName](./get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ImlRenderingMode](./get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_MemoryOptimization](./get_memoryoptimization/)() const | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_PrettyFormat](./get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| virtual [get_SaveFormat](./get_saveformat/)() | Specifies the format in which the document will be saved if this save options object is used. |
| [get_TempFolder](./get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used. |
| [get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/)() const | Gets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](./get_updatefields/)() const | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UseAntiAliasing](./get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](./get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](./set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](./set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](./get_customtimezoneinfo/). |
| [set_DefaultTemplate](./set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](./get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](./set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](./set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](./get_dmlrenderingmode/). |
| [set_ExportGeneratorName](./set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](./get_exportgeneratorname/). |
| [set_ImlRenderingMode](./set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](./get_imlrenderingmode/). |
| [set_MemoryOptimization](./set_memoryoptimization/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_MemoryOptimization](./get_memoryoptimization/). |
| [set_PrettyFormat](./set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](./get_prettyformat/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](./get_progresscallback/). |
| virtual [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) | Setter for [Aspose::Words::Saving::SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateCreatedTimeProperty](./set_updatecreatedtimeproperty/)(bool) | Sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [set_UpdateFields](./set_updatefields/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateFields](./get_updatefields/). |
| [set_UpdateLastPrintedProperty](./set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](./set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/). |
| [set_UseAntiAliasing](./set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](./get_useantialiasing/). |
| [set_UseHighQualityRendering](./set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](./get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Examples



Shows how to use a specific encoding when saving a document to .epub. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
auto saveOptions = MakeObject<HtmlSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions->set_DocumentSplitCriteria(DocumentSplitCriteria::HeadingParagraph);

// Specify that we want to export document properties.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
