---
title: "Aspose::Words::Layout::LayoutCollector 类"
linktitle: "LayoutCollector"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutCollector 类。此类允许计算文档节点的页码。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


此类允许计算文档节点的页码。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。

```cpp
class LayoutCollector : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 清除所有收集的布局数据。在文档手动更新或布局重新构建后调用此方法。 |
| [get_Document](./get_document/)() const | 获取或设置此收集器实例所附加的文档。 |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 获取节点结束所在页面的 1 基索引。如果节点无法映射到页面，则返回 0。 |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回对应于指定节点的 [LayoutEnumerator](../layoutenumerator/) 的不透明位置。给定被枚举的文档与节点的文档相同的情况下，您可以将返回值作为对 [Current](../layoutenumerator/get_current/) 的参数使用。 |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 获取指定节点跨越的页数。如果节点位于单页内则为 0。这与 [GetEndPageIndex()](../) - [GetStartPageIndex()](../) 相同。 |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 获取节点开始所在页的基于 1 的索引。如果节点无法映射到页，则返回 0。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | 初始化此类的实例。 |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | 用于设置 [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/)。 |
| static [Type](./type/)() |  |
## 备注


当您创建 [LayoutCollector](./) 并指定要附加的 [Document](../../aspose.words/document/) 文档对象时，收集器将在文档格式化为页面时记录文档节点到布局对象的映射。

您可以使用 [GetStartPageIndex()](../)、[GetEndPageIndex()](../) 和 [GetNumPagesSpanned()](../) 方法找出特定文档节点（例如 run、段落或表格单元格）所在的页码。这些方法会自动构建文档的页面布局模型，并在需要时更新字段。

当您不再需要收集布局信息时，最好将 [Document](./get_document/) 属性设置为 **null**，以避免不必要的布局映射收集。

## 示例



展示如何查看节点跨越的页面范围。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// 调用 \"GetNumPagesSpanned\" 方法来统计文档内容跨越了多少页。
// 由于文档为空，页数目前为零。
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// 向文档填充 5 页内容。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 在使用布局收集器之前，我们需要调用 \"UpdatePageLayout\" 方法来获取
// 任何布局相关度量的准确数值，例如页数。
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// 我们可以看到任意节点的起始页和结束页的页码以及它们的整体跨页数。
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// 我们可以使用 LayoutEnumerator 迭代布局实体。
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// LayoutEnumerator 可以像树一样遍历布局实体的集合。
// 我们也可以将其应用于任意节点对应的布局实体。
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
