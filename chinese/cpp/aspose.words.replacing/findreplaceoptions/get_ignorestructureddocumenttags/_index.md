---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags 方法。获取或设置一个布尔值，指示是否忽略 StructuredDocumentTag 的内容。默认值在 C++ 中为 false。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


获取或设置一个布尔值，指示是否忽略 [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) 的内容。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## 备注


当此选项设置为 **true** 时，[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) 的内容将被视为普通文本。

否则，[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) 将被视为独立的 [Story](../../../aspose.words/story/)，并且替换模式将在每个 [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) 中分别搜索，这样如果模式跨越了 [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)，则不会对该模式执行替换。

## 示例



展示如何在替换时忽略标签的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// 此段落包含 SDT。
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
