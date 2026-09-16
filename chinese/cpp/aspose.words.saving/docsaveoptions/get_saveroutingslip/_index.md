---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip 方法"
linktitle: "get_SaveRoutingSlip"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip 方法。设置为 false 时，RoutingSlip 数据不会保存到输出文档。默认值在 C++ 中为 true。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.saving/docsaveoptions/get_saveroutingslip/
---
## DocSaveOptions::get_SaveRoutingSlip method


当 **false** 时，RoutingSlip 数据不会保存到输出文档。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SaveRoutingSlip() const
```


## 示例



展示如何为较旧的 Microsoft Word 格式设置保存选项。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// 设置密码，以保护 Microsoft Word 或 Aspose.Words 加载文档时的安全。
// 请注意，这并不会以任何方式加密文档的内容。
options->set_Password(u"MyPassword");

// 如果文档包含流转单，我们可以在保存时通过将此标志设置为 true 来保留它。
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// 为了能够加载文档，
// 我们需要在 LoadOptions 对象中应用我们在 DocSaveOptions 对象中指定的密码。
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
