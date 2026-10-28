---
title: Aspose::Words::Saving::TxtSaveOptions class
linktitle: TxtSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::TxtSaveOptions class. Can be used to specify additional options when saving a document into the Text format. To learn more, visit the Specify Save Options documentation article in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class


Can be used to specify additional options when saving a document into the [Text](../../aspose.words/saveformat/) format. 
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class TxtSaveOptions : public TxtSaveOptionsBase
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [TxtSaveOptions](./txtsaveoptions/)() |  |
| static [Type](./type/)() |  |
| [get_AddBidiMarks](./get_addbidimarks/)() const | Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is **false**. |
| [get_ListIndentation](./get_listindentation/)() const | Gets a [TxtListIndentation](../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels. By default, it is zero count of character '\0', that means no indentation. |
| [get_MaxCharactersPerLine](./get_maxcharactersperline/)() const | Gets or sets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit. |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | Specifies how OfficeMath will be written to the output file. Default value is [Text](../txtofficemathexportmode/). |
| [get_PreserveTableLayout](./get_preservetablelayout/)() const | Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is **false**. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Text](../../aspose.words/saveformat/). |
| [get_SimplifyListLabels](./get_simplifylistlabels/)() const | Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text.

If set to **true**, numbered list labels are written in simple numeric format and itemized list labels as simple ASCII characters. The default value is **false**. |
| [set_AddBidiMarks](./set_addbidimarks/)(bool) | Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is **false**. |
| [set_MaxCharactersPerLine](./set_maxcharactersperline/)(int32_t) | Sets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit. |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::TxtOfficeMathExportMode) | Specifies how OfficeMath will be written to the output file. Default value is [Text](../txtofficemathexportmode/). |
| [set_PreserveTableLayout](./set_preservetablelayout/)(bool) | Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is **false**. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Text](../../aspose.words/saveformat/). |
| [set_SimplifyListLabels](./set_simplifylistlabels/)(bool) | Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text.

If set to **true**, numbered list labels are written in simple numeric format and itemized list labels as simple ASCII characters. The default value is **false**. |
| [GetType](../txtsaveoptionsbase/gettype/)() const override |  |
| [Is](../txtsaveoptionsbase/is/)(const System::TypeInfo \&) const override |  |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](../txtsaveoptionsbase/type/)() |  |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | Specifies the encoding to use when exporting in text formats. Default value is Encoding.UTF8. |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | Specifies the way headers and footers are exported to the text formats. Default value is [PrimaryOnly](../txtexportheadersfootersmode/). |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | Allows to specify whether the page breaks should be preserved during export.

The default value is **false**. |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | Specifies the string to use as a paragraph break when exporting in text formats. |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\> \&) | Specifies the encoding to use when exporting in text formats. Default value is Encoding.UTF8. |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | Specifies the way headers and footers are exported to the text formats. Default value is [PrimaryOnly](../txtexportheadersfootersmode/). |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | Allows to specify whether the page breaks should be preserved during export.

The default value is **false**. |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String \&) | Specifies the string to use as a paragraph break when exporting in text formats. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String \&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [GetType](../saveoptions/gettype/)() const override |  |
| [Is](../saveoptions/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../saveoptions/type/)() |  |
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


Shows how to save a .txt document with a custom paragraph break.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```
## See Also

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
