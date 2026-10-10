---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign 方法"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign 方法。指定是否应将反斜杠字符替换为日元符号。默认值在 C++ 中为 false。"
type: docs
weight: 5500
url: /zh/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


指定是否应将反斜杠字符替换为日元符号。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## 示例



展示如何将反斜杠字符替换为日元符号（Xaml）。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// 默认情况下，Aspose.Words 模仿 MS Word 的行为，不会在
// 生成的 HTML 文档中将反斜杠字符替换为日元符号。然而，Aspose.Words 的早期版本在某些
// 场景下会进行此类替换。此标志启用与 Aspose.Words 早期版本的向后兼容性。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## 另见

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
