---
title: "Aspose::Words::BuildVersionInfo::get_Version 方法"
linktitle: "get_Version"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildVersionInfo::get_Version 方法。获取产品版本，适用于 C++。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


获取产品版本。

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## 备注


产品版本采用 "Major.Minor.Hotfix.0" 格式。

## 示例



展示如何显示已安装的 Aspose.Words 版本信息。
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## 另见

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
