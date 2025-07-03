---
title: Aspose::Words::Saving::OdtSaveOptions class
linktitle: OdtSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OdtSaveOptions class. Can be used to specify additional options when saving a document into the Odt or Ott format. To learn more, visit the  documentation article in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class


Can be used to specify additional options when saving a document into the [Odt](../../aspose.words/saveformat/) or [Ott](../../aspose.words/saveformat/) format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class OdtSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Gets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_IsStrictSchema11](./get_isstrictschema11/)() const | Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is **false**. |
| [get_MeasureUnit](./get_measureunit/)() const | Allows to specify units of measure to apply to document content. The default value is [Centimeters](../odtsavemeasureunit/) |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_Password](./get_password/)() const | Gets or sets a password to encrypt document. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can be [Odt](../../aspose.words/saveformat/) or [Ott](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determines whether the font attributes will be changed according to the character code being used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets or sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdtSaveOptions](./odtsaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the [Odt](../../aspose.words/saveformat/) format. |
| [OdtSaveOptions](./odtsaveoptions/)(const System::String\&) | Initializes a new instance of this class that can be used to save a document in the [Odt](../../aspose.words/saveformat/) format encrypted with a password. |
| [OdtSaveOptions](./odtsaveoptions/)(Aspose::Words::SaveFormat) | Initializes a new instance of this class that can be used to save a document in the [Odt](../../aspose.words/saveformat/) or [Ott](../../aspose.words/saveformat/) format. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::DigitalSignatureDetails\>\&) | Sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_IsStrictSchema11](./set_isstrictschema11/)(bool) | Setter for [Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11](./get_isstrictschema11/). |
| [set_MeasureUnit](./set_measureunit/)(Aspose::Words::Saving::OdtSaveMeasureUnit) | Allows to specify units of measure to apply to document content. The default value is [Centimeters](../odtsavemeasureunit/) |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [set_Password](./set_password/)(const System::String\&) | Setter for [Aspose::Words::Saving::OdtSaveOptions::get_Password](./get_password/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter for [Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |
## Remarks


At the moment provides only the [SaveFormat](./get_saveformat/) property, but in the future will have other options added, such as an encryption password or digital signature settings.

## Examples



Shows how to make a saved document conform to an older ODT schema. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

## See Also

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
