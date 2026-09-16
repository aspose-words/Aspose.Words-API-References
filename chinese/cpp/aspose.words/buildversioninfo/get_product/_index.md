---
title: "Aspose::Words::BuildVersionInfo::get_Product 方法"
linktitle: "get_Product"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildVersionInfo::get_Product 方法。获取产品的完整名称，适用于 C++。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


获取产品的完整名称。

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## 示例



展示如何显示已安装的 Aspose.Words 版本信息。
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## 另见

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
