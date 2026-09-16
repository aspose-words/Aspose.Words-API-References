---
title: "Aspose::Words::Layout::LayoutCollector::GetEntity 方法"
linktitle: "GetEntity"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutCollector::GetEntity 方法。返回与指定节点对应的 LayoutEnumerator 的不透明位置。如果枚举的文档与节点所在的文档相同，您可以将返回值作为参数传递给 Current（在 C++ 中）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


返回与指定节点对应的 [LayoutEnumerator](../../layoutenumerator/) 的不透明位置。如果枚举的文档与节点所在的文档相同，您可以将返回值作为参数传递给 [Current](../../layoutenumerator/get_current/)。

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## 备注


此方法仅适用于 [Paragraph](../../../aspose.words/paragraph/) 节点，以及不可分割的内联节点，例如 [BookmarkStart](../../../aspose.words/bookmarkstart/) 或 [Shape](../../../aspose.words.drawing/shape/)。它不适用于 [Run](../../../aspose.words/run/)、[Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) 或 [Table](../../../aspose.words.tables/table/) 节点，以及页眉/页脚中的节点。

请注意，针对 [Paragraph](../../../aspose.words/paragraph/) 节点返回的实体是段落换行跨度。请使用相应的方法上升到父行。

如果需要导航到文本的 [Run](../../../aspose.words/run/)，可以在其前插入书签，然后导航到该书签。

如果需要导航到 [Cell](../../../aspose.words.tables/cell/) 节点，可以移动到该单元格中的 [Paragraph](../../../aspose.words/paragraph/) 节点，然后上升到父实体。同样的方法可用于 [Row](../../../aspose.words.tables/row/) 和 [Table](../../../aspose.words.tables/table/) 节点。

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

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
