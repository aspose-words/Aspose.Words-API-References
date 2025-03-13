---
title: Aspose::Words::Saving::WordML2003SaveOptions class
linktitle: WordML2003SaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::WordML2003SaveOptions class. Can be used to specify additional options when saving a document into the WordML format. To learn more, visit the  documentation article in C++.'
type: docs
weight: 35000
url: /cpp/aspose.words.saving/wordml2003saveoptions/
---
## WordML2003SaveOptions class


Can be used to specify additional options when saving a document into the [WordML](../../aspose.words/saveformat/) format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class WordML2003SaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [WordML](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determines whether the font attributes will be changed according to the character code being used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_MemoryOptimization](../saveoptions/get_memoryoptimization/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter for [Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Determines whether the font attributes will be changed according to the character code being used. |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateFields](../saveoptions/get_updatefields/). |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |
## Remarks


At the moment provides only the [SaveFormat](./get_saveformat/) property, but in the future may have other options added.

## Examples



Shows how to manage output document's raw content. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
// to modify how we save the document to the WordML save format.
auto options = MakeObject<WordML2003SaveOptions>();

ASSERT_EQ(SaveFormat::WordML, options->get_SaveFormat());

// Set the "PrettyFormat" property to "true" to apply tab character indentation and
// newlines to make the output document's raw content easier to read.
// Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options->set_PrettyFormat(prettyFormat);

doc->Save(ArtifactsDir + u"WordML2003SaveOptions.PrettyFormat.xml", options);

String fileContents = System::IO::File::ReadAllText(ArtifactsDir + u"WordML2003SaveOptions.PrettyFormat.xml");

if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(String(u"<o:DocumentProperties>\r\n\t\t") + u"<o:Revision>1</o:Revision>\r\n\t\t" +
                                      u"<o:TotalTime>0</o:TotalTime>\r\n\t\t" + u"<o:Pages>1</o:Pages>\r\n\t\t" + u"<o:Words>0</o:Words>\r\n\t\t" +
                                      u"<o:Characters>0</o:Characters>\r\n\t\t" + u"<o:Lines>1</o:Lines>\r\n\t\t" +
                                      u"<o:Paragraphs>1</o:Paragraphs>\r\n\t\t" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t" +
                                      u"<o:Version>11.5606</o:Version>\r\n\t" + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") +
                                      u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
                                      u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```


Shows how to manage memory optimization. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
// to modify how we save the document to the WordML save format.
auto options = MakeObject<WordML2003SaveOptions>();

// Set the "MemoryOptimization" flag to "true" to decrease memory consumption
// during the document's saving operation at the cost of a longer saving time.
// Set the "MemoryOptimization" flag to "false" to save the document normally.
options->set_MemoryOptimization(memoryOptimization);

doc->Save(ArtifactsDir + u"WordML2003SaveOptions.MemoryOptimization.xml", options);
```

## See Also

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
