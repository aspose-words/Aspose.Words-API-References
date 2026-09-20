---
title: "Aspose::Words::FileFormatInfo::get_IsEncrypted 方法"
linktitle: "get_IsEncrypted"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatInfo::get_IsEncrypted 方法。若文档已加密且需要密码才能打开，则在 C++ 中返回 true。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


如果文档已加密且需要密码打开，则返回 **true**。

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## 备注


此属性用于帮助您将已加密的文档与未加密的文档进行分类。如果在未提供密码的情况下使用 Aspose.Words 加载加密文档，将抛出异常。您可以使用此属性检测文档是否需要密码，并在加载文档之前采取相应操作，例如提示用户输入密码。

## 示例



展示如何使用 [FileFormatUtil](../../fileformatutil/) 类来检测文档格式和加密情况。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 配置 SaveOptions 对象以加密文档
// 在保存时使用密码，然后保存文档。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// 验证文档的文件类型及其加密状态。
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## 另见

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
