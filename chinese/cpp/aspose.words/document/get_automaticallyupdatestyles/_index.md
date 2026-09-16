---
title: "Aspose::Words::Document::get_AutomaticallyUpdateStyles 方法"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_AutomaticallyUpdateStyles 方法。获取或设置一个标志，指示每次在 C++ 中使用 MS Word 打开文档时，文档中的样式是否会更新以匹配附加模板中的样式。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


获取或设置一个标志，指示每次在 MS Word 中打开文档时，文档中的样式是否更新以匹配附加模板中的样式。

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## 示例



展示如何将模板附加到文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Microsoft Word 文档默认附带一个名为 "Normal.dotm" 的模板。
// 空白的 Aspose.Words 文档没有默认模板。
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// 附加模板，然后设置标志以应用样式更改
// 在模板中将样式应用于我们的文档。
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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
