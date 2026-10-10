---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password 方法"
linktitle: "get_Password"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password 方法。获取/设置用于在 C++ 中使用 ECMA376 标准加密算法加密文档的密码。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


获取/设置用于使用 ECMA376 标准加密算法加密文档的密码。

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## 备注


为了在不加密的情况下保存文档，此属性应为 **null** 或空字符串。

## 示例



展示如何创建密码加密的 Office Open XML 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// 我们将无法使用 Microsoft Word 或
// 在未提供正确密码的情况下打开 Aspose.Words。
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// 通过在 LoadOptions 对象中传入正确的密码来打开加密文档。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
