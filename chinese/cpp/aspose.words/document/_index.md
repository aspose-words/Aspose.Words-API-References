---
title: "Aspose::Words::Document 类"
linktitle: "Document"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document 类。表示一个 Word 文档。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words/document/
---
## Document class


表示一个 Word 文档。要了解更多信息，请访问 [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/) 文档文章。

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptAllRevisions](./acceptallrevisions/)() | 接受文档中所有已跟踪的更改。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问文档的结尾。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问文档的开头。 |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | 将指定的文档追加到此文档的末尾。 |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 将指定的文档追加到此文档的末尾。 |
| [Cleanup](./cleanup/)() | 清除文档中未使用的样式和列表。 |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | 根据给定的 [CleanupOptions](../cleanupoptions/) 清除文档中未使用的样式和列表。 |
| [Clone](./clone/)() | 对 [Document](./) 执行深度复制。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | 将此文档与另一个文档进行比较，生成编辑和格式修订次数的更改 [Revision](../revision/)。 |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 将此文档与另一个文档进行比较，生成作为编辑和格式修订的更改 [Revision](../revision/)。允许使用 [CompareOptions](../../aspose.words.comparing/compareoptions/) 指定比较选项。 |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | 将指定模板中的样式复制到文档中。 |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | 将指定模板中的样式复制到文档中。 |
| [Document](./document/)() | 创建一个空白的 Word 文档。 |
| [Document](./document/)(const System::String\&) | 从文件打开现有文档。自动检测文件格式。 |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 从文件打开现有文档。允许指定附加选项，例如加密密码。 |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | 从流打开现有文档。自动检测文件格式。 |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 从流打开现有文档。允许指定附加选项，例如加密密码。 |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | 如果文档不包含任何节，则创建一个包含一个段落的节。 |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | 将表格样式中指定的格式转换为文档中表格的直接格式。 |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | 返回表示指定页面范围和给定页面提取选项的 [Document](./) 对象。 |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | 返回表示指定页面范围的 [Document](./) 对象。 |
| [get_AttachedTemplate](./get_attachedtemplate/)() | 获取或设置附加到文档的模板的完整路径。 |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | 获取或设置一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配附加模板中的样式。 |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | 获取或设置文档的背景形状。可以为 **null**。 |
| [get_Bibliography](./get_bibliography/)() | 获取表示文档中可用来源列表的 [Bibliography](./get_bibliography/) 对象。 |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | 返回表示文档所有内置属性的集合。 |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | 提供对文档兼容性选项的访问（即在 Word 的 **Options** 对话框的 **Compatibility** 选项卡中输入的用户首选项）。 |
| [get_Compliance](./get_compliance/)() | 获取从加载的文档内容确定的 OOXML 合规版本。仅对 OOXML 文档有意义。 |
| [get_Count](../compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | 返回表示文档所有自定义属性的集合。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_CustomXmlParts](./get_customxmlparts/)() const | 获取或设置自定义 XML 数据存储部件的集合。 |
| [get_DefaultTabStop](./get_defaulttabstop/)() | 获取或设置默认制表位之间的间隔（以点为单位）。 |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | 获取此文档的数字签名集合及其验证结果。 |
| [get_Document](../documentbase/get_document/)() const override | 获取此实例。 |
| [get_EndnoteOptions](./get_endnoteoptions/)() | 提供控制本文档中尾注编号和位置的选项。 |
| [get_FieldOptions](./get_fieldoptions/)() | 获取表示控制文档中字段处理选项的 [FieldOptions](../../aspose.words.fields/fieldoptions/) 对象。 |
| [get_FirstChild](../compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstSection](./get_firstsection/)() | 获取文档中的第一节。 |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | 提供对本文件中使用的字体属性的访问。 |
| [get_FontSettings](./get_fontsettings/)() const | 获取或设置文档字体设置。 |
| [get_FootnoteOptions](./get_footnoteoptions/)() | 提供控制本文件中脚注编号和位置的选项。 |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | 提供对文档中定义的脚注/尾注分隔符的访问。 |
| [get_Frameset](./get_frameset/)() const | 如果此文档表示一个框架页面，则返回一个 [Frameset](./get_frameset/) 实例。 |
| [get_GlossaryDocument](./get_glossarydocument/)() const | 获取或设置此文档或模板中的词汇文档。词汇文档是用于存储在文档中定义的 AutoText、AutoCorrect 和 Building Block 条目的存储区。 |
| [get_GrammarChecked](./get_grammarchecked/)() | 如果已对文档进行语法检查，则返回 **true**。 |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_HasMacros](./get_hasmacros/)() | 如果文档具有 VBA 项目（宏），则返回 **true**。 |
| [get_HasRevisions](./get_hasrevisions/)() | 如果文档有任何已跟踪的更改，则返回 **true**。 |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | 提供对文档连字符选项的访问。 |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | 指定是否在字数统计中包括文本框、脚注和尾注。 |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_JustificationMode](./get_justificationmode/)() | 获取或设置文档的字符间距调整。 |
| [get_LastChild](../compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_LastSection](./get_lastsection/)() | 获取文档中的最后一节。 |
| [get_LayoutOptions](./get_layoutoptions/)() const | 获取一个表示控制此文档布局过程的选项的 [LayoutOptions](../../aspose.words.layout/layoutoptions/) 对象。 |
| [get_Lists](../documentbase/get_lists/)() const | 提供对文档中使用的列表格式的访问。 |
| [get_MailMerge](./get_mailmerge/)() | 返回一个表示文档邮件合并功能的 [MailMerge](../../aspose.words.mailmerging/mailmerge/) 对象。 |
| [get_MailMergeSettings](./get_mailmergesettings/)() | 获取或设置包含文档所有邮件合并信息的对象。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | 当在文档中插入或删除节点时调用。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Document](../nodetype/)。 |
| [get_OriginalFileName](./get_originalfilename/)() const | 获取文档的原始文件名。 |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | 获取加载到此对象中的原始文档的格式。 |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | 获取或设置使用 "unknown relationships" 链接到 OOXML 包的自定义部件（任意内容）集合。 |
| [get_PageColor](../documentbase/get_pagecolor/)() | 获取或设置文档的页面颜色。此属性是 [BackgroundShape](../documentbase/get_backgroundshape/) 的简化版本。 |
| [get_PageCount](./get_pagecount/)() | 获取文档的页数，该页数由最近的页面布局操作计算得出。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | 获取当前活动的文档保护类型。 |
| [get_PunctuationKerning](./get_punctuationkerning/)() | 指定字距调整是否同时适用于拉丁文本和标点符号。 |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | 提供文档的可读性评分信息。 |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | 获取或设置一个标志，指示 Microsoft Word 在保存文档时将删除评论、修订和文档属性中的所有用户信息。 |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | 允许控制外部资源的加载方式。 |
| [get_Revisions](./get_revisions/)() | 获取此文档中存在的修订（已跟踪更改）集合。 |
| [get_RevisionsView](./get_revisionsview/)() const | 获取或设置一个值，指示是使用文档的原始版本还是修订版本。 |
| [get_Sections](./get_sections/)() | 返回表示文档中所有章节的集合。 |
| [get_ShadeFormData](./get_shadeformdata/)() | 指定是否在表单字段上启用灰色阴影。 |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | 指定是否在此文档中显示语法错误。 |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | 指定是否在此文档中显示拼写错误。 |
| [get_SpellingChecked](./get_spellingchecked/)() | 如果文档已进行拼写检查，则返回 **true**。 |
| [get_Styles](../documentbase/get_styles/)() const | 返回文档中定义的样式集合。 |
| [get_Theme](./get_theme/)() | 获取此文档的 [Theme](./get_theme/) 对象。 |
| [get_TrackRevisions](./get_trackrevisions/)() | 如果在 Microsoft Word 中编辑此文档时跟踪更改，则为 True。 |
| [get_Variables](./get_variables/)() | 返回添加到文档或模板的变量集合。 |
| [get_VbaProject](./get_vbaproject/)() const | 获取或设置一个 [VbaProject](./get_vbaproject/)。 |
| [get_VersionsCount](./get_versionscount/)() | 获取存储在 DOC 文档中的文档版本数量。 |
| [get_ViewOptions](./get_viewoptions/)() | 提供选项以控制文档在 Microsoft Word 中的显示方式。 |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | 在各种文档处理过程中调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| [get_Watermark](./get_watermark/)() | 提供对文档水印的访问。 |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | 返回表示任务窗格加载项列表的集合。 |
| [get_WriteProtection](./get_writeprotection/)() | 提供对文档写保护选项的访问。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetPageInfo](./getpageinfo/)(int32_t) | 获取页面尺寸、方向以及可能对打印或渲染有用的其他页面信息。 |
| [GetText](../compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 将另一个文档的节点导入到当前文档。 |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | 合并文档中所有段落中具有相同格式的运行。 |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | 更改整个文档中 [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) 的字段类型值，针对 [FieldStart](../../aspose.words.fields/fieldstart/)、[FieldSeparator](../../aspose.words.fields/fieldseparator/)、[FieldEnd](../../aspose.words.fields/fieldend/) ，使其对应于字段代码中包含的字段类型。 |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | 在不更改现有密码的情况下保护文档免受更改，或分配一个随机密码。 |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | 保护文档免受更改，并可选地设置保护密码。 |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveBlankPages](./removeblankpages/)() | 从文档中删除空白页。 |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | 从文档中删除工具栏和键盘命令的自定义。 |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | 从此文档中删除外部 XML 架构引用。 |
| [RemoveMacros](./removemacros/)() | 从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义。 |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | 将文档页面渲染到 **Graphics** 对象，使用指定的比例。 |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | 将文档页面渲染到 **Graphics** 对象，使用指定的尺寸。 |
| [Save](./save/)(const System::String\&) | 将文档保存到文件。自动根据扩展名确定保存格式。 |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | 以指定格式将文档保存到文件。 |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将文档保存到文件。 |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 使用指定的格式将文档保存到流中。 |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将文档保存到流中。 |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | 选择匹配 XPath 表达式的第一个 [Node](../node/)。 |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/) 的 setter。 |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | 用于设置 [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/) 的 setter。 |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | 用于设置 [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/) 的 setter。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | 用于设置 [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/) 的 setter。 |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | 用于设置 [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/) 的 setter。 |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 用于设置 [Aspose::Words::Document::get_FontSettings](./get_fontsettings/) 的 setter。 |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | 用于设置 [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/) 的 setter。 |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | 用于设置 [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/) 的 setter。 |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | 用于设置 [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/) 的 setter。 |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | 用于设置 [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/)。 |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | 用于设置 [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/)。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | 当在文档中插入或删除节点时调用。 |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | 用于设置 [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/)。 |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/)。 |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | 用于设置 [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/)。 |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | 用于设置 [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/)。 |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | 允许控制外部资源的加载方式。 |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | 用于设置 [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/)。 |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | 用于设置 [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/)。 |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | 用于设置 [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)。 |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | 用于设置 [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/)。 |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | 用于设置 [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/)。 |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | 用于设置 [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/)。 |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | 用于设置 [Aspose::Words::Document::get_VbaProject](./get_vbaproject/)。 |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 用于设置 [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/)。 |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | 自动开始将您对文档所做的所有后续更改标记为修订更改。 |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | 自动开始将您对文档所做的所有后续更改标记为修订更改。 |
| [StopTrackRevisions](./stoptrackrevisions/)() | 停止自动将文档更改标记为修订。 |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | 取消链接文档中的所有字段。 |
| [Unprotect](./unprotect/)() | 无论密码如何，都移除文档的保护。 |
| [Unprotect](./unprotect/)(const System::String\&) | 如果指定了正确的密码，则移除文档的保护。 |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | 更新文档中所有脚注和尾注的 [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) 属性。 |
| [UpdateFields](./updatefields/)() | 更新整个文档中字段的值。 |
| [UpdateListLabels](./updatelistlabels/)() | 更新文档中所有列表项的列表标签。 |
| [UpdatePageLayout](./updatepagelayout/)() | 重新构建文档的页面布局。 |
| [UpdateTableLayout](./updatetablelayout/)() | 实现了一种早期的表列宽重新计算方法，但已知存在问题。 |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | 根据指定的选项更新文档的 [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/)。 |
| [UpdateThumbnail](./updatethumbnail/)() | 使用默认选项更新文档的[Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/)。 |
| [UpdateWordCount](./updatewordcount/)() | 更新文档的字数统计属性。 |
| [UpdateWordCount](./updatewordcount/)(bool) | 更新文档的字数统计属性，可选地更新[Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/)属性。 |
## 备注


[Document](./) 是 Aspose.Words 库的核心对象。

要在任意[LoadFormat](../loadformat/)格式中加载现有文档，请将文件名或流传入其中一个[Document](./)构造函数。要创建空白文档，请在不传入参数的情况下调用构造函数。

使用 Save 方法的重载之一，将文档保存为任意[SaveFormat](../saveformat/)格式。

要将文档页面直接绘制到 **Graphics** 对象上，请使用 [RenderToScale()](../) 或 [RenderToSize()](../) 方法。

要打印文档，请使用其中一个 [Print()](../) 方法。

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

[Document](./) 是包含文档所有其他节点的树的根节点。该树采用组合设计模式，在许多方面类似于 XmlDocument。文档的内容可以通过编程自由操作：

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



考虑使用 [DocumentBuilder](../documentbuilder/)，它简化了以编程方式创建或填充文档树的任务。

[Document](./) 只能包含 [Section](../section/) 对象。

在 Microsoft Word 中，有效文档必须至少包含一个节。
## 另见

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
