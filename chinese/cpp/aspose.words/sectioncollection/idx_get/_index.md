---
title: "Aspose::Words::SectionCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SectionCollection::idx_get 方法。在 C++ 中检索给定索引处的节。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


检索给定索引处的节。

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 节列表中的索引。 |
## 备注


索引从零开始。

允许使用负索引，并表示从集合的末尾访问。例如 -1 表示最后一个项目，-2 表示倒数第二个，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

## 示例



显示何时重新计算文档的页面布局。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 首次将文档保存为 PDF、图像或打印时，将自动
// 缓存文档在各页中的布局。
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// 在当前版本的 Aspose.Words 中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望缓存的布局
// 保持最新，需要手动更新。
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```


展示如何准备一个新的节节点以进行编辑。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 一个空白文档自带一个节，该节有一个正文，正文中又包含一个段落。
// 我们可以通过向该段落添加文本运行、形状或表格等元素来向此文档添加内容。
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// 如果我们这样添加一个新节，它将没有正文或任何其他子节点。
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 运行 "EnsureMinimum" 方法，为此节添加正文和段落，以开始编辑。
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
