---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password 方法"
linktitle: "get_Password"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password 方法。获取或设置用于在 C++ 中加密文档的密码。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


获取或设置用于加密文档的密码。

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## 备注


为了在不加密的情况下保存文档，此属性应为 **null** 或空字符串。

## 示例



展示如何使用密码加密已保存的 ODT/OTT 文档，然后使用 Aspose.Words 加载它。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 创建一个新的 OdtSaveOptions，并传入 "SaveFormat.Odt",
// 或 "SaveFormat.Ott" 作为文档保存的格式。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// 如果我们使用合适的编辑器打开此文档，
// 它将提示我们输入在 SaveOptions 对象中指定的密码。
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// 如果我们希望再次使用 Aspose.Words 打开或编辑此文档，
// 我们必须在加载构造函数中提供包含正确密码的 LoadOptions 对象。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## 另见

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
