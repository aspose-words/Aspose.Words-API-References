---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag 方法"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag 方法。获取当前在此 DocumentBuilder 中选中的结构化文档标签（C++）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


获取当前在此 [DocumentBuilder](../) 中选中的结构化文档标签。

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
```


## 示例



展示如何使用 [DocumentBuilder](../) 将光标移动到结构化文档标签内部。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 有多种方式可以移动光标：
// 1 -  通过索引移动到结构化文档标签的第一个字符。
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  通过对象移动到结构化文档标签的第一个字符。
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  移动到第二个结构化文档标签的末尾。
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// 获取当前选中的结构化文档标签。
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## 另见

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
