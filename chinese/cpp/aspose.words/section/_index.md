---
title: "Aspose::Words::Section class"
linktitle: "Section"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Section class. 表示文档中的单个节。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words/section/
---
## Section class


表示文档中的单个章节。要了解更多，请访问 [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) 文档文章。

```cpp
class Section : public Aspose::Words::CompositeNode,
                public Aspose::Words::ISectionAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 当在派生类中实现时，调用指定文档访问器的 VisitXXXEnd 方法。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 当在派生类中实现时，调用指定文档访问器的 VisitXXXStart 方法。 |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendContent](./appendcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | 在此节的末尾插入源节内容的副本。 |
| [ClearContent](./clearcontent/)() | 清除该节。 |
| [ClearHeadersFooters](./clearheadersfooters/)() | 清除该节的页眉和页脚。 |
| [ClearHeadersFooters](./clearheadersfooters/)(bool) | 清除该节的页眉和页脚。 |
| [Clone](./clone/)() | 创建该节的副本。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [DeleteHeaderFooterShapes](./deleteheaderfootershapes/)() | 删除该节页眉和页脚中的所有形状（绘图对象）。 |
| [EnsureMinimum](./ensureminimum/)() | 确保该节具有 [Body](./get_body/) 且包含一个 [Paragraph](../paragraph/)。 |
| [get_Body](./get_body/)() | 返回该节的 [Body](../body/) 子节点。 |
| [get_Count](../compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](../compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_HeadersFooters](./get_headersfooters/)() | 提供对节的页眉和页脚节点的访问。 |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](../compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Section](../nodetype/)。 |
| [get_PageSetup](./get_pagesetup/)() | 返回一个表示页面设置和节属性的对象。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectedForForms](./get_protectedforforms/)() | 如果节已对表单受保护则为 True。当节对表单受保护时，用户只能在 Microsoft Word 中的表单字段中选择和修改文本。 |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](../compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PrependContent](./prependcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | 在此节的开头插入源节内容的副本。 |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [Section](./section/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | 初始化一个新的 [Section](./) 类实例。 |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | 选择匹配 XPath 表达式的第一个 [Node](../node/)。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ProtectedForForms](./set_protectedforforms/)(bool) | 用于设置 [Aspose::Words::Section::get_ProtectedForForms](./get_protectedforforms/) 的 setter。 |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[Section](./) can have one [Body](../body/) and maximum one [HeaderFooter](../headerfooter/) of each [HeaderFooterType](../headerfootertype/). [Body](../body/) and [HeaderFooter](../headerfooter/) nodes can be in any order inside [Section](./).

一个最小的有效节需要有 [Body](../body/) 并包含一个 [Paragraph](../paragraph/)。

每个节都有自己的一组属性，用于指定页面大小、方向、边距等。

您可以使用 [Clone()](../node/clone/) 创建节的副本。该副本可以插入到相同或不同的文档中。

要添加、插入或删除整个节（包括节分隔符和节属性），请使用 [Sections](../document/get_sections/) 对象的方法。

要复制并插入仅节的内容（不包括节分隔符和节属性），请使用 [AppendContent()](../) 和 [PrependContent()](../) 方法。

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
