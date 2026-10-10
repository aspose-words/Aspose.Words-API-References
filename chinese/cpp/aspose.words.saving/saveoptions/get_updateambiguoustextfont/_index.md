---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont 方法"
linktitle: "get_UpdateAmbiguousTextFont"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont 方法。确定在 C++ 中是否会根据所使用的字符代码更改字体属性。"
type: docs
weight: 15500
url: /zh/cpp/aspose.words.saving/saveoptions/get_updateambiguoustextfont/
---
## SaveOptions::get_UpdateAmbiguousTextFont method


确定字体属性是否会根据所使用的字符代码进行更改。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont() const
```


## 示例



展示如何更新字体以匹配所使用的字符代码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Special symbol.docx");
System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Arial

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateAmbiguousTextFont(true);
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Angsana New
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
