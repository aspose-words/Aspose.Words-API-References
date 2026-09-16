---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate 方法"
linktitle: "get_DefaultTemplate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate 方法。获取或设置默认模板的路径（包括文件名）。此属性在 C++ 中的默认值为空字符串。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


获取或设置默认模板的路径（包括文件名）。此属性的默认值为 **empty string**。

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


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

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
