---
title: "Aspose::Words::FileFormatUtil::ExtensionToSaveFormat 方法"
linktitle: "ExtensionToSaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatUtil::ExtensionToSaveFormat 方法。将文件扩展名转换为 C++ 中的 SaveFormat 值。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil::ExtensionToSaveFormat method


将文件扩展名转换为 [SaveFormat](../../saveformat/) 值。

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(const System::String &extension)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 扩展名 | const System::String\& | 文件扩展名。可以带或不带前导点。大小写不敏感。 |
## 备注


如果无法识别该扩展名，返回 [Unknown](../../saveformat/)。

## 示例



展示如何使用 [FileFormatUtil](../) 方法检测文档的格式。
```cpp
// 从缺少文件扩展名的文件加载文档，然后检测其文件格式。
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // 下面是将 LoadFormat 转换为相应 SaveFormat 的两种方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - 直接将 LoadFormat 转换为其 SaveFormat：
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // 从流中加载文档，然后保存为自动检测的文件扩展名。
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## 另见

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
