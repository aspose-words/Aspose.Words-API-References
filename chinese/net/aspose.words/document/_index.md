---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Document 类，实现无缝 Word 文档操作。强大的功能和便捷的集成将增强您的项目。
type: docs
weight: 640
url: /zh/net/aspose.words/document/
---
## Document class

代表 Word 文档。

要了解更多信息，请访问[使用文档](https://docs.aspose.com/words/net/working-with-document/)文档文章。

```csharp
public class Document : DocumentBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Document](document/#constructor)() | 创建一个空白的 Word 文档。 |
| [Document](document/#constructor_1)(*Stream*) | 从流中打开现有文档。自动检测文件格式。 |
| [Document](document/#constructor_3)(*string*) | 从文件中打开现有文档。自动检测文件格式。 |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 从流中打开现有文档。允许指定其他选项，例如加密密码。 |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 从文件中打开现有文档。允许指定其他选项，例如加密密码。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | 获取或设置附加到文档的模板的完整路径。 |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | 获取或设置一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配 附加模板中的样式。 |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | 获取或设置文档的背景形状。可以是`无效的`. |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | 获取[`Bibliography`](./bibliography/)表示文档中可用源列表的对象。 |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | 返回代表文档所有内置文档属性的集合。 |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | 提供对文档兼容性选项的访问（即在**兼容性** 标签**选项**Word 中的对话框）。 |
| [Compliance](../../aspose.words/document/compliance/) { get; } | 获取根据加载的文档内容确定的 OOXML 合规版本。 仅对 OOXML 文档有意义。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | 返回代表文档的所有自定义文档属性的集合。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | 获取或设置自定义 XML 数据存储部分的集合。 |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | 获取或设置默认制表位之间的间隔（以点为单位）。 |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | 获取此文档的数字签名集合及其验证结果。 |
| override [Document](../../aspose.words/documentbase/document/) { get; } | 获取此实例。 |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | 提供控制本文档中尾注编号和定位的选项。 |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | 获得[`FieldOptions`](../../aspose.words.fields/fieldoptions/)表示控制文档中字段处理的选项的对象。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | 获取文档中的第一部分。 |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | 提供对本文档中使用的字体属性的访问。 |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | 获取或设置文档字体设置。 |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | 提供控制本文档中脚注编号和定位的选项。 |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | 提供对文档中定义的脚注/尾注分隔符的访问。 |
| [Frameset](../../aspose.words/document/frameset/) { get; } | 返回[`Frameset`](./frameset/)例如，如果此文档代表一个框架页面。 |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | 获取或设置此文档或模板中的词汇表文档。词汇表文档是文档中定义的自动图文集、自动更正和构建基块条目的存储单元。 |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | 返回`真的`如果文档已经检查过语法。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | 返回`真的`如果文档有一个 VBA 项目（宏）. |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | 返回`真的`如果文档有任何跟踪修订。 |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | 提供对文档连字选项的访问。 |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | 指定是否在字数统计中包含文本框、脚注和尾注。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | 获取或设置文档的字符间距调整。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | 获取文档中的最后一部分。 |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | 获得[`LayoutOptions`](../../aspose.words.layout/layoutoptions/)表示控制此文档布局过程的选项的对象。 |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | 提供对文档中使用的列表格式的访问。 |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | 返回[`MailMerge`](../../aspose.words.mailmerging/mailmerge/)表示文档的邮件合并功能的对象。 |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | 获取或设置包含文档所有邮件合并信息的对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | 在文档中插入或删除节点时调用。 |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | 返回Document. |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | 获取文档的原始文件名。 |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | 获取加载到此对象的原始文档的格式。 |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | 获取或设置使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。 |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | 获取或设置文档的页面颜色。此属性是[`BackgroundShape`](../documentbase/backgroundshape/). |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | 获取最近一次页面布局操作计算出的文档页数。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | 获取当前活动的文档保护类型。 |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | 指定字距调整是否适用于拉丁文本和标点符号。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | 获取或设置一个标志，指示 Microsoft Word 将在保存文档时从注释、修订和文档属性中删除所有用户信息。 |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | 允许控制如何加载外部资源。 |
| [Revisions](../../aspose.words/document/revisions/) { get; } | 获取此文档中存在的修订（跟踪的更改）的集合。 |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | 获取或设置一个值，指示是否使用文档的原始版本或修订版本。 |
| [Sections](../../aspose.words/document/sections/) { get; } | 返回代表文档中所有部分的集合。 |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | 指定是否打开表单字段上的灰色阴影。 |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | 指定是否显示此文档中的语法错误。 |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | 指定是否显示此文档中的拼写错误。 |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | 返回`真的`如果文档已经过拼写检查。 |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | 返回文档中定义的样式集合。 |
| [Theme](../../aspose.words/document/theme/) { get; } | 获取[`Theme`](./theme/)此文档的对象。 |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | 如果在 Microsoft Word 中编辑此文档时跟踪更改，则为 True。 |
| [Variables](../../aspose.words/document/variables/) { get; } | 返回添加到文档或模板的变量集合。 |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | 获取或设置[`VbaProject`](./vbaproject/). |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | 获取 DOC 文档中存储的文档版本数。 |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | 提供选项来控制文档在 Microsoft Word 中的显示方式。 |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | 在各种文档处理过程中，当检测到可能导致数据或格式保真度损失的问题时调用。 |
| [Watermark](../../aspose.words/document/watermark/) { get; } | 提供对文档水印的访问。 |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | 返回代表任务窗格加载项列表的集合。 |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | 提供对文档写保护选项的访问。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | 接受文档中的所有修订。 |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访问者访问文档末尾。 |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访问者访问文档的开头。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | 将指定文档附加到此文档的末尾。 |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | 将指定文档附加到此文档的末尾。 |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | 清除文档中未使用的样式和列表。 |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | 根据给定的条件清除文档中未使用的样式和列表[`CleanupOptions`](../cleanupoptions/). |
| [Clone](../../aspose.words/document/clone/#clone)() | 执行深层复制`Document`. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | 将此文档与另一个文档进行比较，得出编辑次数和格式修订的变化[`Revision`](../revision/). |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 将此文档与另一文档进行比较，产生许多编辑和格式修订[`Revision`](../revision/). 允许使用指定比较选项[`CompareOptions`](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | 将样式从指定的模板复制到文档。 |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | 将样式从指定的模板复制到文档。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | 如果文档不包含任何章节，则创建一个包含一个段落的章节。 |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | 将表格样式中指定的格式转换为文档中表格的直接格式。 |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | 返回`Document`表示指定页面范围的对象。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | 获取页面大小、方向和其他可能对打印或渲染有用的页面信息。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | 将节点从另一个文档导入到当前文档。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | 将文档所有段落中具有相同格式的文本合并。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | 更改字段类型值[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/)的[`FieldStart`](../../aspose.words.fields/fieldstart/)，[`FieldSeparator`](../../aspose.words.fields/fieldseparator/)，[`FieldEnd`](../../aspose.words.fields/fieldend/) 在整个文档中，以便它们与字段代码中包含的字段类型相对应。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Print](../../aspose.words/document/print/#print)() | 将整个文档打印到默认打印机。 |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | 根据指定的打印机设置打印文档， 使用标准（无用户界面）打印控制器。 |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | 将整个文档打印到指定的打印机， 使用标准（无用户界面）打印控制器。 |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | 根据指定的打印机设置打印文档， 使用标准（无用户界面）打印控制器和文档名称。 |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | 保护文档不被更改，无需更改现有密码或分配随机密码。 |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | 保护文档不被更改，并可选择设置保护密码。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | 从文档中删除空白页。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | 从此文档中删除外部 XML 架构引用。 |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | 从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | 将文档页面渲染为Graphics对象到指定的比例。 |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | 将文档页面渲染为Graphics对象到指定的大小。 |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | 将文档保存为文件。根据扩展名自动确定保存格式。 |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | 使用指定格式将文档保存到流。 |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将文档保存到流中。 |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | 将文档保存为指定格式的文件。 |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将文档保存到文件。 |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 将文档发送到客户端浏览器。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | 开始自动将您对文档所做的所有进一步更改以编程方式标记为修订更改。 |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | 开始自动将您对文档所做的所有进一步更改以编程方式标记为修订更改。 |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | 停止自动将文档更改标记为修订。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | 取消整个文档中的字段链接。 |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | 无论密码是什么，都会删除文档的保护。 |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | 如果指定了正确的密码，则删除文档的保护。 |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | 更新[`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/)文档中所有脚注和尾注的属性。 |
| [UpdateFields](../../aspose.words/document/updatefields/)() | 更新整个文档中字段的值。 |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | 更新文档中所有列表项的列表标签。 |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | 重建文档的页面布局。 |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | 更新[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/)使用默认选项的文档。 |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | 更新[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/)根据指定的选项对文档进行修改。 |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | 更新文档的字数属性。 |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | 更新文档的字数属性，可选更新[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/)属性. |

## 评论

这`Document`是 Aspose.Words 库中的核心对象。

要加载现有文档，请执行以下操作之一：[`LoadFormat`](../loadformat/)格式，将文件名 或流传递到其中之一`Document`构造函数。要创建空白文档，请调用不带参数的 构造函数。

使用 Save 方法重载之一将文档保存在任意 [`SaveFormat`](../saveformat/)格式。

将文档页面直接绘制到**图形**对象 use [`RenderToScale`](./rendertoscale/)或者[`RenderToSize`](./rendertosize/)方法。

要打印文档，请使用[`Print`](./print/)方法。

[`MailMerge`](./mailmerge/)是 Aspose.Words 的报告引擎，允许使用来自各种数据源的数据快速轻松地填充在 Microsoft Word 中设计的 报告。 数据可以来自 DataSet、DataTable、DataView、IDataReader 或值数组。 **邮件合并**将遍历数据源中找到的记录，并根据需要将其插入到文档中的 邮件合并字段中，以扩大文档的规模。

`Document`存储文档范围的信息，例如[`Styles`](../documentbase/styles/), [`BuiltInDocumentProperties`](./builtindocumentproperties/)，[`CustomDocumentProperties`](./customdocumentproperties/)、列表和宏。 大多数这些对象都可以通过相应的属性访问`Document`。

这`Document`是包含文档所有其他节点的树的根节点。 该树是一种复合设计模式，在许多方面类似于 XmlDocument。 可以通过编程自由操作文档的内容：

* 可以通过类型集合访问文档的节点，例如[`Sections`](./sections/), [`ParagraphCollection`](../paragraphcollection/) ETC。
* 可以使用 通过节点类型来选择文档的节点[`GetChildNodes`](../compositenode/getchildnodes/) 或使用 XPath 查询[`SelectNodes`](../compositenode/selectnodes/)或者[`SelectSingleNode`](../compositenode/selectsinglenode/)。
* 可以使用 在文档的任何位置添加或删除内容节点[`InsertBefore`](../compositenode/insertbefore/)，[`InsertAfter`](../compositenode/insertafter/), [`RemoveChild`](../compositenode/removechild/)以及基类提供的 other 方法[`CompositeNode`](../compositenode/)。
* 每个节点的格式属性可以通过该节点的属性进行更改。

考虑使用[`DocumentBuilder`](../documentbuilder/)这简化了以编程方式创建 或填充文档树的任务。

这`Document`仅可包含[`Section`](../section/)对象。

在 Microsoft Word 中，有效文档至少需要有一个部分。

## 例子

展示如何使用 DataTable 中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 以下是使用 DataTable 作为邮件合并数据源的两种方法。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - 使用表的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// 创建邮件合并源文档。
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### 也可以看看

* class [DocumentBase](../documentbase/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
