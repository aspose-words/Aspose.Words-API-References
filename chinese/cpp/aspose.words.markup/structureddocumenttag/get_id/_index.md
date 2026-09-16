---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Id 方法"
linktitle: "get_Id"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Id 方法。指定此 SDT 在 C++ 中的唯一只读持久数值 Id。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


为此 **SDT** 指定唯一的只读持久数值 Id。

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## 备注


Id 属性应遵循以下规则：* 仅当整个文档被克隆时，文档才会保留 SDT id [Clone](../../../aspose.words/document/clone/)。
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



## 示例



展示如何在纯文本框中创建结构化文档标签并修改其外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个将包含纯文本的结构化文档标签。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// 设置当在 Microsoft Word 中将鼠标悬停在结构化文档标签上时出现的框架的标题和颜色。
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// 为此结构化文档标签设置一个可获取的标签。
// 作为名为 "tag" 的 XML 元素，在其 "@val" 属性中放置以下字符串。
tag->set_Tag(u"MyPlainTextSDT");

// 每个结构化文档标签都有一个随机唯一的 ID。
ASSERT_TRUE(tag->get_Id() > 0);

// 设置结构化文档标签内部文本的字体。
tag->get_ContentsFont()->set_Name(u"Arial");

// 设置结构化文档标签末尾文本的字体。
// 使用方向键移出标签后，在文档正文中输入的任何文本都将使用此字体。
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// 默认情况下，此值为 false，在结构化文档标签内部按回车键不会产生任何操作。
// 设置为 true 时，我们的结构化文档标签可以包含多行。

// 将 "Multiline" 属性设置为 "false" 以仅允许内容
// 此结构化文档标签的内容仅跨越单行。
// 将 "Multiline" 属性设置为 "true" 以允许标签包含多行内容。
tag->set_Multiline(true);

// 将 "Appearance" 属性设置为 "SdtAppearance.Tags" 以在内容周围显示标签。
// 默认情况下，结构化文档标签显示为 BoundingBox。
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// 在新段落中插入我们结构化文档标签的克隆。
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// 使用 "RemoveSelfOnly" 方法删除结构化文档标签，同时保留其在文档中的内容。
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## 另见

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
