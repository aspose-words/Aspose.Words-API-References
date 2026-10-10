---
title: "Aspose::Words::FileFormatInfo::get_HasMacros 方法"
linktitle: "get_HasMacros"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatInfo::get_HasMacros 方法。若文档包含 VBA 宏，则在 C++ 中返回 true。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words/fileformatinfo/get_hasmacros/
---
## FileFormatInfo::get_HasMacros method


如果此文档包含 VBA 宏，则返回 **true**。

```cpp
bool Aspose::Words::FileFormatInfo::get_HasMacros() const
```


## 示例



展示如何在不加载文档的情况下检查 VBA 宏的存在。
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> fileFormatInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Macro.docm");
ASSERT_TRUE(fileFormatInfo->get_HasMacros());
```

## 另见

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
