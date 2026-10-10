---
title: "Aspose::Words::Saving::TxtSaveOptions 类"
linktitle: "TxtSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptions 类。可用于在将文档保存为 Text 格式时指定其他选项。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class


可用于在将文档保存为 [Text](../../aspose.words/saveformat/) 格式时指定其他选项。欲了解更多，请访问 [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) 文档文章。

```cpp
class TxtSaveOptions : public Aspose::Words::Saving::TxtSaveOptionsBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | 创建一个适用于指定保存格式的保存选项对象。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | 创建一个适用于给定文件名中指定的文件扩展名的保存选项对象。 |
| [get_AddBidiMarks](./get_addbidimarks/)() const | 指定在以纯文本格式导出时是否在每个 BiDi 运行前添加双向标记。默认值为 **false**。 |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | 获取或设置一个布尔值，指示在文档保存时是否允许在嵌入 TrueType 字体时嵌入带有 PostScript 描边的字体。默认值为 **false**。 |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | 获取或设置默认模板的路径（包括文件名）。此属性的默认值为 **empty string**。 |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 获取决定 3D 效果渲染方式的值。 |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | 获取或设置决定 DrawingML 效果渲染方式的值。 |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | 获取或设置决定 DrawingML 形状渲染方式的值。 |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | 指定在文本格式导出时使用的编码。默认值为 **Encoding.UTF8**。 |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | 当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。 |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | 指定页眉和页脚导出到文本格式的方式。默认值为 [PrimaryOnly](../txtexportheadersfootersmode/)。 |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | 允许指定在导出时是否应保留分页符。默认值为 **false**。 |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | 获取或设置决定墨水 (InkML) 对象渲染方式的值。 |
| [get_ListIndentation](./get_listindentation/)() const | 获取一个 [TxtListIndentation](../txtlistindentation/) 对象，用于指定列表级别缩进使用的字符数量和类型。默认情况下，它是字符 '\\0' 的零计数，这意味着没有缩进。 |
| [get_MaxCharactersPerLine](./get_maxcharactersperline/)() const | 获取或设置一个整数值，指定每行的最大字符数。默认值为 0，这意味着无限制。 |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | 获取决定在保存文档之前是否执行内存优化的值。此属性的默认值为 **false**。 |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | 指定 OfficeMath 将如何写入输出文件。默认值为 [Text](../txtofficemathexportmode/)。 |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | 指定在文本格式导出时用作段落换行的字符串。 |
| [get_PreserveTableLayout](./get_preservetablelayout/)() const | 指定程序在以纯文本格式保存时是否尝试保留表格布局。默认值为 **false**。 |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | 当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。 |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | 在保存文档期间调用，并接受有关保存进度的数据。 |
| [get_SaveFormat](./get_saveformat/)() override | 指定在使用此保存选项对象时文档将保存的格式。只能是 [Text](../../aspose.words/saveformat/)。 |
| [get_SimplifyListLabels](./get_simplifylistlabels/)() const | 指定程序在纯文本无法充分表示复杂标签格式时是否应简化列表标签。若设置为 **true**，编号列表标签将以简单的数字格式写入，项目符号列表标签则使用简单的 ASCII 字符。默认值为 **false**。 |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | 指定在保存为 DOC 或 DOCX 文件时使用的临时文件夹。默认情况下，此属性为 **null**，且不使用临时文件。 |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | 确定字体属性是否会根据所使用的字符代码进行更改。 |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) 属性的值。默认值为 **false**；。 |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | 获取决定在将文档保存为固定页面格式之前是否应更新某些类型字段的值。此属性的默认值为 **true**。 |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | 获取或设置决定在保存前是否更新 [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) 属性的值。 |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) 属性的值。 |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | 获取一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | 获取或设置一个值，用于确定是否在渲染时使用抗锯齿。 |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | 获取或设置一个值，用于确定是否使用高质量（即慢速）的渲染算法。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddBidiMarks](./set_addbidimarks/)(bool) | 用于设置 [Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks](./get_addbidimarks/) 的方法。 |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) 的 setter。 |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) 的 setter。 |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) 的 setter。 |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 设置一个值，用于确定 3D 效果的渲染方式。 |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/) 的 setter。 |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/) 的 setter。 |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | 用于设置 [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](../txtsaveoptionsbase/get_encoding/) 的 setter。 |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/) 的 setter。 |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | 用于设置 [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/) 的 setter。 |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | 用于设置 [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/) 的 setter。 |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)。 |
| [set_MaxCharactersPerLine](./set_maxcharactersperline/)(int32_t) | 用于设置 [Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine](./get_maxcharactersperline/) 的方法。 |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | 设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为 **false**。 |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::TxtOfficeMathExportMode) | 用于设置 [Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode](./get_officemathexportmode/) 的方法。 |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/) 的 setter。 |
| [set_PreserveTableLayout](./set_preservetablelayout/)(bool) | 用于设置 [Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout](./get_preservetablelayout/) 的方法。 |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/)。 |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/) 的 setter。 |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | 用于设置 [Aspose::Words::Saving::TxtSaveOptions::get_SaveFormat](./get_saveformat/) 的方法。 |
| [set_SimplifyListLabels](./set_simplifylistlabels/)(bool) | 用于设置 [Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels](./get_simplifylistlabels/) 的方法。 |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/) 的 setter。 |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/) 的 setter。 |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/) 的 setter。 |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | 设置一个值，用于确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为 **true**。 |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/) 的 setter。 |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/) 的 setter。 |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | 设置一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/) 的 setter。 |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/) 的 setter。 |
| [TxtSaveOptions](./txtsaveoptions/)() |  |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |

## 示例



展示如何使用自定义段落换行保存 .txt 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");
builder->Write(u"Paragraph 3.");

// 创建一个 "TxtSaveOptions" 对象，可将其传递给文档的 "Save" 方法
// 以修改我们保存文档为纯文本的方式。
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Text, txtSaveOptions->get_SaveFormat());

// 将 "ParagraphBreak" 设置为我们希望放在每个段落末尾的自定义值。
txtSaveOptions->set_ParagraphBreak(u" End of paragraph.\n\n\t");

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ParagraphBreak.txt");

ASSERT_EQ(System::String(u"Paragraph 1. End of paragraph.\n\n\t") + u"Paragraph 2. End of paragraph.\n\n\t" + u"Paragraph 3. End of paragraph.\n\n\t", docText);
```

## 另见

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
