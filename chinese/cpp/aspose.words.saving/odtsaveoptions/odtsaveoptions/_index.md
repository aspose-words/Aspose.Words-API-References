---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions 构造函数"
linktitle: "OdtSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions 构造函数。初始化此类的新实例，可用于在 C++ 中以 Odt 格式保存文档。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


初始化此类的新实例，可用于以 [Odt](../../../aspose.words/saveformat/) 格式保存文档。

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## 示例



展示如何使已保存的文档符合旧的 ODT 架构。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## 另见

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


初始化此类的新实例，可用于以 [Odt](../../../aspose.words/saveformat/) 或 [Ott](../../../aspose.words/saveformat/) 格式保存文档。

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | 可以是 [Odt](../../../aspose.words/saveformat/) 或 [Ott](../../../aspose.words/saveformat/)。 |

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
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


初始化此类的新实例，可用于以带密码加密的 [Odt](../../../aspose.words/saveformat/) 格式保存文档。

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## 另见

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
