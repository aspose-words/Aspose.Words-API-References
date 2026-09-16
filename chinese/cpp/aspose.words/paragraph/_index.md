---
title: "Aspose::Words::Paragraph 类"
linktitle: "段落"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph 类。表示一段文本。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 47000
url: /zh/cpp/aspose.words/paragraph/
---
## Paragraph class


表示一段文本。要了解更多，请访问 [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) 文档文章。

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问文档段落的结尾。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问文档段落的起始。 |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | 向此段落追加字段。 |
| [AppendField](./appendfield/)(const System::String\&) | 向此段落追加字段。 |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | 向此段落追加字段。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | 如果此段落换行是 [Style](../style/) 分隔符，则为 True。样式分隔符允许一个段落由具有不同段落样式的部分组成。 |
| [get_Count](../compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](../compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FrameFormat](./get_frameformat/)() | 提供对框架格式属性的访问。 |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsEndOfCell](./get_isendofcell/)() | 如果此段落是 [Cell](../../aspose.words.tables/cell/) 中的最后一个段落，则为 True；否则为 False。 |
| [get_IsEndOfDocument](./get_isendofdocument/)() | 如果此段落是文档最后一个章节中的最后一个段落，则为 True。 |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | 如果此段落是 [Section](../section/) 的 [HeaderFooter](../headerfooter/)（主文本故事）中的最后一个段落，则为 True；否则为 False。 |
| [get_IsEndOfSection](./get_isendofsection/)() | 如果此段落是 [Section](../section/) 的 [Body](../body/)（主文本故事）中的最后一个段落，则为 True；否则为 False。 |
| [get_IsFormatRevision](./get_isformatrevision/)() | 如果在启用更改跟踪时，Microsoft Word 中对象的格式被更改，则返回 true。 |
| [get_IsInCell](./get_isincell/)() | 如果此段落是 [Cell](../../aspose.words.tables/cell/) 的直接子项，则为 True；否则为 False。 |
| [get_IsInsertRevision](./get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsListItem](./get_islistitem/)() | 当段落在原始修订中是项目符号或编号列表的项时，为 True。 |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_LastChild](../compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_ListFormat](./get_listformat/)() | 提供对段落列表格式属性的访问。 |
| [get_ListLabel](./get_listlabel/)() | 获取一个 [ListLabel](./get_listlabel/) 对象，该对象提供对本段落的列表编号值和格式的访问。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Paragraph](../nodetype/)。 |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | 提供对段落换行字符的字体格式的访问。 |
| [get_ParagraphFormat](./get_paragraphformat/)() | 提供对段落格式属性的访问。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentSection](./get_parentsection/)() | 检索段落的父级 [Section](../section/)。 |
| [get_ParentStory](./get_parentstory/)() | 检索父级章节级别的故事，可为 [Body](../body/) 或 [HeaderFooter](../headerfooter/)。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [get_Runs](./get_runs/)() | 提供对段落内部文本片段的强类型集合的访问。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | 返回应用于此段落的所有制表位数组，包括通过样式或列表间接应用的制表位。 |
| [GetEnumerator](../compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](./gettext/)() override | 获取此段落的文本，包括段落结束字符。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 在此段落中插入字段。 |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 在此段落中插入字段。 |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 在此段落中插入字段。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | 合并段落中具有相同格式的运行。 |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | 合并段落中具有相同格式的运行。 |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | 初始化一个新的 [Paragraph](./) 类实例。 |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | 选择匹配 XPath 表达式的第一个 [Node](../node/)。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

段落中可能出现的子节点完整列表包括 [BookmarkStart](../bookmarkstart/)、[BookmarkEnd](../bookmarkend/)、[FieldStart](../../aspose.words.fields/fieldstart/)、[FieldSeparator](../../aspose.words.fields/fieldseparator/)、[FieldEnd](../../aspose.words.fields/fieldend/)、[FormField](../../aspose.words.fields/formfield/)、[Comment](../comment/)、[Footnote](../../aspose.words.notes/footnote/)、[Run](../run/)、[SpecialChar](../specialchar/)、[Shape](../../aspose.words.drawing/shape/)、[GroupShape](../../aspose.words.drawing/groupshape/)、[SmartTag](../../aspose.words.markup/smarttag/)。

Microsoft Word 中有效的段落始终以段落换行符结束，最小的有效段落仅由段落换行符组成。 [Paragraph](./) 类会自动在末尾追加适当的段落换行符，并且该字符不属于 [Paragraph](./) 的子节点，因此 [Paragraph](./) 可以为空。

不要在段落文本中包含段落结束符 [ParagraphBreak](../controlchar/paragraphbreak/) 或单元格结束符 [Cell](../controlchar/cell/) ，否则在 Microsoft Word 中打开文档时可能导致段落无效。

## 示例



展示如何手动构建 Aspose.Words 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 空白文档包含一个节、一个主体和一个段落。
// 调用 "RemoveAllChildren" 方法以删除所有这些节点，
// 最终得到一个没有子节点的文档节点。
doc->RemoveAllChildren();

// 此文档现在没有可用于添加内容的复合子节点。
// 如果我们想编辑它，需要重新填充其节点集合。
// 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// 为该节设置一些页面布局属性。
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// 一个节需要一个主体，用于包含并显示其所有内容
// 在页面上位于该节的页眉和页脚之间。
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// 创建一个段落，设置一些格式属性，然后将其作为子节点追加到主体中。
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// 最后，添加一些内容以完成文档。创建一个运行（run），
// 设置其外观和内容，然后将其作为子节点追加到段落中。
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## 另见

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
