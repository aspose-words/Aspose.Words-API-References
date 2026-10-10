---
title: "Aspose::Words::FileFormatUtil::LoadFormatToExtension 方法"
linktitle: "LoadFormatToExtension"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatUtil::LoadFormatToExtension 方法。将加载格式枚举值转换为文件扩展名。返回的扩展名是在 C++ 中带前导点的小写字符串。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil::LoadFormatToExtension method


将加载格式枚举值转换为文件扩展名。返回的扩展名是带前导点的小写字符串。

```cpp
static System::String Aspose::Words::FileFormatUtil::LoadFormatToExtension(Aspose::Words::LoadFormat loadFormat)
```

## 备注


该 [WordML](../../saveformat/) 值被转换为 \".wml\"。

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

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
