---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary 方法"
linktitle: "get_IsTemporary"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary 方法。指定当其内容在 C++ 中被修改时，是否应从 WordProcessingML 文档中移除此 SDT。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


指定当其内容被修改时，是否应从 WordProcessingML 文档中移除此 **SDT**。

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## 示例



展示如何创建一次性使用的控件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 插入一个纯文本结构化文档标签，
// 它将充当一个纯文本表单，用户可以在其中输入文本。
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// 将 "IsTemporary" 属性设置为 "true"，使结构化文档标签消失并
// 在用户在 Microsoft Word 中编辑一次后，将其内容合并到文档中。
// 将 "IsTemporary" 属性设置为 "false"，以允许用户编辑内容
// 结构化文档标签的内容任意次数。
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// 插入另一个以复选框形式的结构化文档标签，并将其默认状态设置为 "已选中"。
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// 将 "IsTemporary" 属性设置为 "true"，使复选框变成符号
// 一旦用户在 Microsoft Word 中点击它。
// 将 "IsTemporary" 属性设置为 "false"，允许用户任意次数点击复选框。
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## 另见

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
