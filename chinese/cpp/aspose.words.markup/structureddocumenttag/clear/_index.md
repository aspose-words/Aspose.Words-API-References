---
title: "Aspose::Words::Markup::StructuredDocumentTag::Clear 方法"
linktitle: "清除"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::Clear 方法。清除此结构化文档标签的内容，并在 C++ 中如果已定义则显示占位符。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


清除此结构化文档标签的内容，并在已定义时显示占位符。

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## 备注


如果结构化文档标签有修订，则无法清除其内容。

如果此结构化文档标签映射到自定义 XML（使用 [XmlMapping](../get_xmlmapping/) 属性），则引用的 XML 节点将被清除。

## 示例



展示如何删除结构化文档标签元素的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个纯文本结构化文档标签，然后将其追加到文档中。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// 此结构化文档标签以文本框形式呈现，已经显示占位符文本。
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// 创建一个包含文本内容的构建块。
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// 将结构化文档标签的 "PlaceholderName" 属性设置为我们的构建块名称，以获取
// 结构化文档标签显示构建块的内容，以替代原始默认文本。
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// 编辑结构化文档标签的文本并隐藏占位符文本。
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// 使用 "Clear" 方法清除此结构化文档标签的内容并再次显示占位符。
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## 另见

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
