---
title: "Aspose::Words::Layout::LayoutCollector::LayoutCollector 构造函数"
linktitle: "LayoutCollector"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutCollector::LayoutCollector 构造函数。在 C++ 中初始化此类的实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.layout/layoutcollector/layoutcollector/
---
## LayoutCollector::LayoutCollector constructor


初始化此类的实例。

```cpp
Aspose::Words::Layout::LayoutCollector::LayoutCollector(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::Document\>\& | 此收集器实例将附加到的文档。 |

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

* Class [Document](../../../aspose.words/document/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
