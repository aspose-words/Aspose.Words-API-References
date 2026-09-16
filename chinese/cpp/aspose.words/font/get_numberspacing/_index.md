---
title: "Aspose::Words::Font::get_NumberSpacing 方法"
linktitle: "get_NumberSpacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_NumberSpacing 方法。获取或设置在 C++ 中显示的数字的间距类型。"
type: docs
weight: 30500
url: /zh/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


获取或设置所显示数字的间距类型。

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## 示例



展示如何设置数字的间距类型。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 此效果仅在较新版本的 MS Word 中受支持。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## 另见

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
