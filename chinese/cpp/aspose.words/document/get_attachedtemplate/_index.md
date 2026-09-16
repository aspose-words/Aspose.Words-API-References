---
title: "Aspose::Words::Document::get_AttachedTemplate 方法"
linktitle: "get_AttachedTemplate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_AttachedTemplate 方法。获取或设置文档在 C++ 中所附加模板的完整路径。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


获取或设置附加到文档的模板的完整路径。

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## 备注


空字符串表示文档附加的是 Normal 模板。

## 示例



展示如何为没有附加模板的文档设置默认模板。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 启用自动样式更新，但不附加模板文档。
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// 由于没有模板文档，文档无法跟踪样式更改。
// 使用 SaveOptions 对象自动设置模板
// 如果我们正在保存的文档没有模板。
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
