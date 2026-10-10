---
title: "Aspose::Words::FileFormatInfo::get_Encoding 方法"
linktitle: "get_Encoding"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatInfo::get_Encoding 方法。获取当前文档格式（如果适用）的检测到的编码。目前仅在 C++ 中对 HTML 文档检测编码。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


获取检测到的编码（如果适用于当前文档格式）。目前仅对 HTML 文档检测编码。

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## 示例



展示如何检测 html 文件的编码。
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Encoding 属性仅在我们为 html 文档创建 FileFormatInfo 对象时使用。
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## 另见

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
