---
title: "Aspose::Words::Settings::ViewOptions::get_FormsDesign 方法"
linktitle: "get_FormsDesign"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewOptions::get_FormsDesign 方法。指定文档在 C++ 中是否处于表单设计模式。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.settings/viewoptions/get_formsdesign/
---
## ViewOptions::get_FormsDesign method


指定文档是否处于表单设计模式。

```cpp
bool Aspose::Words::Settings::ViewOptions::get_FormsDesign() const
```

## 备注


当前仅适用于 WordML 格式的文档。

## 示例



展示如何启用/禁用表单设计模式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 将 "FormsDesign" 属性设置为 "false" 以保持表单设计模式禁用。
// 将 "FormsDesign" 属性设置为 "true" 以启用表单设计模式。
doc->get_ViewOptions()->set_FormsDesign(useFormsDesign);

doc->Save(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml");

ASPOSE_ASSERT_EQ(useFormsDesign, System::IO::File::ReadAllText(get_ArtifactsDir() + u"ViewOptions.FormsDesign.xml").Contains(u"<w:formsDesign />"));
```

## 另见

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
