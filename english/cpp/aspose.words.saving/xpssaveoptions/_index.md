---
title: Aspose::Words::Saving::XpsSaveOptions class
linktitle: XpsSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XpsSaveOptions class. Can be used to specify additional options when saving a document into the Xps format. To learn more, visit the Specify Save Options documentation article in C++.'
type: docs
weight: 38000
url: /cpp/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class


Can be used to specify additional options when saving a document into the [Xps](../../aspose.words/saveformat/) format. 
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class XpsSaveOptions : public FixedPageSaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| [XpsSaveOptions](./xpssaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the [Xps](../../aspose.words/saveformat/) format. |
| [XpsSaveOptions](./xpssaveoptions/)(Aspose::Words::SaveFormat) | Initializes a new instance of this class that can be used to save a document in the [Xps](../../aspose.words/saveformat/) or [OpenXps](../../aspose.words/saveformat/) format. |
| [get_CompressionLevel](./get_compressionlevel/)() const | Specifies the compression level used to save document. The default value is [Normal](../compressionlevel/). |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Gets or sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Allows to specify outline options. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Xps](../../aspose.words/saveformat/). |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [set_CompressionLevel](./set_compressionlevel/)(Aspose::Words::Saving::CompressionLevel) | Specifies the compression level used to save document. The default value is [Normal](../compressionlevel/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::DigitalSignatureDetails\> \&) | Sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Xps](../../aspose.words/saveformat/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Gets or sets a value determining how colors are rendered. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Gets or sets a value determining the quality of the JPEG images inside Html document. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Allows to specify metafile rendering options. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **false**. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Gets or sets the pages to render. Default is all the pages in the document. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Sets a value determining how colors are rendered. |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Sets a value determining the quality of the JPEG images inside Html document. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\> \&) | Allows to specify metafile rendering options. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **false**. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\> \&) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\> \&) | Sets the pages to render. Default is all the pages in the document. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String \&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is empty string. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets or sets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| virtual [get_SaveFormat](../saveoptions/get_saveformat/)() | Specifies the format in which the document will be saved if this save options object is used. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is **null** and no temporary files are used. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determines whether the font attributes will be changed according to the character code being used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets or sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Gets a value determining whether OLE controls presentation image will be updated. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\> \&) | Sets custom local time zone used for date/time fields. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String \&) | Sets path to default template (including filename). Default value for this property is empty string. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Sets a value determining how DrawingML effects are rendered. |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Sets a value determining how DrawingML shapes are rendered. |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Sets a value determining how ink (InkML) objects are rendered. |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | When **true**, pretty formats output where applicable. Default value is **false**. |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\> \&) | Called during saving a document and accepts data about saving progress. |
| virtual [set_SaveFormat](../saveoptions/set_saveformat/)(Aspose::Words::SaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String \&) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is **null** and no temporary files are used. |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Determines whether the font attributes will be changed according to the character code being used. |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**; |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Sets a value determining whether OLE controls presentation image will be updated. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
## Examples


Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(SaveFormat::Xps, saveOptions->get_SaveFormat());

// The output XPS document will contain an outline, a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```
## See Also

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
