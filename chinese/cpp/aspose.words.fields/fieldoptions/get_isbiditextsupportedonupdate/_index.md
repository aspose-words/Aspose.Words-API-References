---
title: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate 方法"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate 方法。获取或设置指示在字段更新期间是否完全支持双向文本的值（C++）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


获取或设置指示在字段更新期间是否完全支持双向文本的值。

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## 备注


当此属性设置为 **true** 时，会执行额外步骤，以在更新期间生成兼容从右到左语言（例如阿拉伯语或希伯来语）的字段结果。

当此属性设置为 **false** 且使用从右到左语言时，字段更新后的结果正确性无法保证。

默认值为 **false**。

## 示例



展示如何使用 [FieldOptions](../) 来确保字段更新完全支持双向文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 确保任何涉及从右到左文本的字段操作都按预期执行。
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// 使用文档生成器插入包含从右到左文本的字段。
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## 另见

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
