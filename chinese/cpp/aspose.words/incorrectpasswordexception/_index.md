---
title: "Aspose::Words::IncorrectPasswordException typedef"
linktitle: "IncorrectPasswordException"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IncorrectPasswordException typedef。若文档使用密码加密，而在打开文档时指定的密码不正确或缺失，则会抛出此异常。欲了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 134000
url: /zh/cpp/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException typedef


如果文档使用密码加密且打开文档时指定的密码不正确或缺失，则抛出此异常。要了解更多，请访问[Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/)文档文章。

```cpp
using Aspose::Words::IncorrectPasswordException = typedef System::ExceptionWrapper<Details_IncorrectPasswordException>
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
