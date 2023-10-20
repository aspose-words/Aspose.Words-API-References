---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Document 班级. 代表 Word 文档 在 C#.
type: docs
weight: 430
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
| [Document](document/#constructor)() | 创建一个空白 Word 文档。 |
| [Document](document/#constructor_1)(*Stream*) | 从流中打开现有文档。自动检测文件格式。 |
| [Document](document/#constructor_3)(*string*) | 从文件中打开现有文档。自动检测文件格式。 |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 从流中打开现有文档。允许指定其他选项，例如加密密码。 |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 从文件中打开现有文档。允许指定其他选项，例如加密密码。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | 获取或设置附加到文档的模板的完整路径。 |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | 获取或设置一个标志，指示每次在 MS Word 中打开文档时是否更新文档中的样式以匹配 附加模板中的样式。 |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | 获取或设置文档的背景形状。可`无效的`. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | 返回一个集合，表示文档的所有内置文档属性。 |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | 提供对文档兼容性选项的访问（即在文档上输入的用户首选项）**兼容性** 选项卡**选项**Word 中的对话框）. |
| [Compliance](../../aspose.words/document/compliance/) { get; } | 获取根据加载的文档内容确定的 OOXML 合规版本。 仅对 OOXML 文档有意义。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | 返回表示文档的所有自定义文档属性的集合。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | 获取或设置自定义 XML 数据存储部分的集合。 |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | 获取或设置默认制表位之间的间隔（以磅为单位）。 |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | 获取此文档的数字签名及其验证结果的集合。 |
| override [Document](../../aspose.words/documentbase/document/) { get; } | 获取此实例。 |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | 提供控制本文档中尾注的编号和位置的选项。 |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | 获得[`FieldOptions`](../../aspose.words.fields/fieldoptions/)表示控制文档中字段处理的选项的对象。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | 获取文档中的第一部分。 |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | 提供对本文档中使用的字体属性的访问。 |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | 获取或设置文档字体设置。 |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | 提供控制本文档中脚注的编号和位置的选项。 |
| [Frameset](../../aspose.words/document/frameset/) { get; } | 返回一个[`Frameset`](./frameset/)实例，如果该文档代表一个框架页面。 |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | 获取或设置此文档或模板中的术语表文档。词汇表文档是文档中定义的自动图文集、自动更正和构建块条目的存储 。 |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | 返回`真的`如果文档已经过语法检查。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | 返回`真的`如果文档有 VBA 项目（宏）. |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | 返回`真的`文档是否有任何跟踪更改。 |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | 提供对文档连字符选项的访问。 |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | 指定字数统计中是否包括文本框、脚注和尾注。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | 获取或设置文档的字符间距调整。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | 获取文档中的最后一部分。 |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | 获得[`LayoutOptions`](../../aspose.words.layout/layoutoptions/)表示控制此文档布局过程的选项的对象。 |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | 提供对文档中使用的列表格式的访问。 |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | 返回一个[`MailMerge`](../../aspose.words.mailmerging/mailmerge/)代表文档邮件合并功能的对象。 |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | 获取或设置包含文档的所有邮件合并信息的对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | 在文档中插入或删除节点时调用。 |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | 返回Document. |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | 获取文档的原始文件名。 |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | 获取加载到此对象中的原始文档的格式。 |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | 获取或设置使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。 |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | 获取或设置文档的页面颜色。这个属性是一个更简单的版本[`BackgroundShape`](../documentbase/backgroundshape/). |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | 获取通过最近的页面布局操作计算得出的文档中的页数。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | 获取当前活动的文档保护类型。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | 获取或设置一个标志，指示 Microsoft Word 在保存文档时将从注释、修订和 文档属性中删除所有用户信息。 |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | 允许控制如何加载外部资源。 |
| [Revisions](../../aspose.words/document/revisions/) { get; } | 获取此文档中存在的修订（跟踪更改）的集合。 |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | 获取或设置一个值，该值指示是否使用文档的原始版本或修订版本。 |
| [Sections](../../aspose.words/document/sections/) { get; } | 返回表示文档中所有部分的集合。 |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | 指定是否打开表单字段上的灰色底纹。 |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | 指定是否显示本文档中的语法错误。 |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | 指定是否显示本文档中的拼写错误。 |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | 返回`真的`如果文档已经过拼写检查。 |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | 返回文档中定义的样式集合。 |
| [Theme](../../aspose.words/document/theme/) { get; } | 获取[`Theme`](./theme/)本文档的对象. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | 如果在 Microsoft Word 中编辑此文档时跟踪更改，则为 True。 |
| [Variables](../../aspose.words/document/variables/) { get; } | 返回添加到文档或模板的变量集合。 |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | 获取或设置[`VbaProject`](./vbaproject/). |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | 获取 DOC 文档中存储的文档版本数。 |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | 提供控制文档在 Microsoft Word 中显示方式的选项。 |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | 在检测到可能导致 数据或格式保真度损失的问题时在各种文档处理过程中调用。 |
| [Watermark](../../aspose.words/document/watermark/) { get; } | 提供对文档水印的访问。 |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | 返回表示任务窗格加载项列表的集合。 |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | 提供对文档写保护选项的访问。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | 接受文档中所有跟踪的更改。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | 将指定文档追加到该文档的末尾。 |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | 将指定文档追加到该文档的末尾。 |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | 从文档中清除未使用的样式和列表。 |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | 根据给定的条件从文档中清除未使用的样式和列表[`CleanupOptions`](../cleanupoptions/). |
| [Clone](../../aspose.words/document/clone/#clone)() | 执行深度复制`Document`. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | 将此文档与另一个文档进行比较，产生编辑和格式修订次数等更改[`Revision`](../revision/). |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | 将此文档与另一个文档进行比较，产生一些编辑和格式修订的更改[`Revision`](../revision/). 允许使用指定比较选项[`CompareOptions`](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | 将样式从指定模板复制到文档。 |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | 将样式从指定模板复制到文档。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | 如果文档不包含任何节，则创建一个包含一个段落的节。 |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | 将表格样式中指定的格式转换为文档中表格的直接格式。 |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | 返回`Document`代表指定页面范围的对象。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | 获取可能对打印或渲染有用的页面大小、方向和其他信息。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | 将节点从另一个文档导入到当前文档。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之后立即插入指定的节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之前插入指定的节点。 |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | 在文档的所有段落中以相同的格式连接运行。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | 更改字段类型值[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/)的[`FieldStart`](../../aspose.words.fields/fieldstart/),[`FieldSeparator`](../../aspose.words.fields/fieldseparator/),[`FieldEnd`](../../aspose.words.fields/fieldend/) 在整个文档中，以便它们对应于字段代码中包含的字段类型。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取前一个节点。 |
| [Print](../../aspose.words/document/print/#print)() | 将整个文档打印到默认打印机。 |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | 根据指定的打印机设置打印文档， 使用标准（无用户界面）打印控制器。 |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | 使用标准（无用户界面）打印控制器将整个文档打印到指定打印机。 |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | 根据指定的打印机设置打印文档， 使用标准（无用户界面）打印控制器和文档名称。 |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | 保护文档免遭更改，而不更改现有密码或分配随机密码。 |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | 保护文档免遭更改，并可选择设置保护密码。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | 删除指定的子节点。 |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | 从此文档中删除外部 XML 架构引用。 |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | 从文档中删除所有宏（VBA 项目）以及工具栏和命令自定义。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | 将文档页面呈现为Graphics指定比例的对象。 |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | 将文档页面呈现为Graphics指定大小的对象。 |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | 将文档保存到文件。自动根据扩展名确定保存格式。 |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | 使用指定格式将文档保存到流。 |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将文档保存到流。 |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | 将文档保存到指定格式的文件中。 |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将文档保存到文件。 |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | 将文档发送到客户端浏览器。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | 开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。 |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | 开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。 |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | 停止将文档更改自动标记为修订版。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出到字符串中。 |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | 取消链接整个文档中的字段。 |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | 无论密码如何，都会删除文档的保护。 |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | 如果指定了正确的密码，则删除文档的保护。 |
| [UpdateFields](../../aspose.words/document/updatefields/)() | 更新整个文档中的字段值。 |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | 更新文档中所有列表项的列表标签。 |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | 重建文档的页面布局。 |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | 更新[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/)使用默认选项的文档。 |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | 更新[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/)根据指定选项的文档。 |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | 更新文档的字数统计属性。 |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | 更新文档的字数统计属性，可选择更新[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/)属性. |

## 评论

这`Document`是 Aspose.Words 库中的核心对象。

要加载任何现有文档[`LoadFormat`](../loadformat/)格式，将文件名 或流传递到其中之一`Document`构造函数。要创建空白文档，请调用不带参数的 构造函数。

使用 Save 方法重载之一将文档保存在任何 the 中[`SaveFormat`](../saveformat/)格式。

将文档页面直接绘制到**图形**对象 use [`RenderToScale`](./rendertoscale/)或者[`RenderToSize`](./rendertosize/)方法。

要打印文档，请使用其中之一[`Print`](./print/)方法。

[`MailMerge`](./mailmerge/)是 Aspose.Words 的报告引擎，允许快速轻松地使用来自各种数据源的数据填充在 Microsoft Word 中设计的 报告。 数据可以来自 DataSet、DataTable、DataView、IDataReader 或值数组。 **邮件合并**将遍历数据源中找到的记录，并根据需要将它们插入到文档中的 邮件合并字段中。

`Document`存储文档范围的信息，例如[`Styles`](../documentbase/styles/), [`BuiltInDocumentProperties`](./builtindocumentproperties/),[`CustomDocumentProperties`](./customdocumentproperties/)、列表和宏。 这些对象中的大多数都可以通过`Document`。

这`Document`是包含文档所有其他节点的树的根节点。 该树是复合设计模式，在许多方面类似于 XmlDocument。 可以通过编程方式自由操作文档的内容：

* 文档的节点可以通过类型化集合来访问，例如[`Sections`](./sections/), [`ParagraphCollection`](../paragraphcollection/) ETC。
* 文档的节点可以通过其节点类型使用 来选择[`GetChildNodes`](../compositenode/getchildnodes/) 或使用 XPath 查询[`SelectNodes`](../compositenode/selectnodes/)或者[`SelectSingleNode`](../compositenode/selectsinglenode/)。
* 可以使用 在文档中的任何位置添加或删除内容节点[`InsertBefore`](../compositenode/insertbefore/),[`InsertAfter`](../compositenode/insertafter/), [`RemoveChild`](../compositenode/removechild/)以及基类提供的 other 方法[`CompositeNode`](../compositenode/)。
* 每个节点的格式属性可以通过该节点的属性来更改。

考虑使用[`DocumentBuilder`](../documentbuilder/)这简化了以编程方式创建 或填充文档树的任务。

这`Document`只能包含[`Section`](../section/)对象。

在 Microsoft Word 中，一份有效的文档需要至少有一个部分。

## 例子

演示如何使用数据表中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 下面是使用 DataTable 作为邮件合并数据源的两种方法。
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
