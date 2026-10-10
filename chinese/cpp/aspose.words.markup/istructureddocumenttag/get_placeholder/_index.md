---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Placeholder 方法"
linktitle: "get_Placeholder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Placeholder 方法。获取包含占位符文本的 BuildingBlock，当此 SDT 的运行内容为空、通过 XmlMapping 元素指定的关联映射 XML 元素为空，或 IsShowingPlaceholderText 元素为 true 时，应显示该文本（在 C++ 中）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.markup/istructureddocumenttag/get_placeholder/
---
## IStructuredDocumentTag::get_Placeholder method


获取包含占位符文本的 [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)，当此 SDT 的运行内容为空、通过 [XmlMapping](../get_xmlmapping/) 元素指定的关联映射 XML 元素为空，或 [IsShowingPlaceholderText](../get_isshowingplaceholdertext/) 元素为 true 时，应显示该文本。

```cpp
virtual System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::Markup::IStructuredDocumentTag::get_Placeholder()=0
```


## 示例



展示如何将构建块的内容用作结构化文档标签的自定义占位符文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入一个类型为 "PlainText" 的纯文本结构化文档标签，它将充当文本框。
// 它默认显示的内容是一个 "Click here to enter text." 提示。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// 我们可以让标签显示构建块的内容，而不是默认文本。
// 首先，向词汇文档中添加一个包含内容的构建块。
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// 然后，使用结构化文档标签的 "PlaceholderName" 属性按名称引用该构建块。
tag->set_PlaceholderName(u"Custom Placeholder");

// 如果 "PlaceholderName" 引用父文档词汇文档中已有的块，
// 我们将能够通过 "Placeholder" 属性验证该构建块。
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// 将 "IsShowingPlaceholderText" 属性设置为 "true" 以将
// 结构化文档标签的当前内容视为占位符文本。
// 这意味着在 Microsoft Word 中单击文本框时，会立即突出显示标签的所有内容。
// 将 "IsShowingPlaceholderText" 属性设置为 "false" 以获取
// 结构化文档标签将其内容视为用户已经输入的文本。
// 在 Microsoft Word 中单击此文本会将闪烁的光标放置在所单击的位置。
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## 另见

* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
