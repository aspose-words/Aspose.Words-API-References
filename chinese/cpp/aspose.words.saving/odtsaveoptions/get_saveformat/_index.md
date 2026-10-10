---
title: "Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat 方法"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat 方法。指定在使用此保存选项对象时文档将保存的格式。可在 C++ 中为 Odt 或 Ott。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/odtsaveoptions/get_saveformat/
---
## OdtSaveOptions::get_SaveFormat method


指定在使用此保存选项对象时文档将保存的格式。可为 [Odt](../../../aspose.words/saveformat/) 或 [Ott](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
