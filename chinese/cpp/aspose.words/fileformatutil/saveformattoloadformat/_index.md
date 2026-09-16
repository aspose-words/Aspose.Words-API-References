---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat 方法"
linktitle: "SaveFormatToLoadFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat 方法。 如果可能，在 C++ 中将 SaveFormat 值转换为 LoadFormat 值。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


如果可能，将 [SaveFormat](../../saveformat/) 值转换为 [LoadFormat](../../loadformat/) 值。

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## 示例



展示如何将保存格式转换为其对应的加载格式。
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// 使用 Aspose.Words 时，某些文件类型可以保存文档，但无法加载。
// 如果我们尝试将此类的保存格式转换为加载格式，将抛出异常。
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## 另见

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
