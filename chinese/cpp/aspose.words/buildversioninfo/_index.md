---
title: "Aspose::Words::BuildVersionInfo 类"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildVersionInfo class. 提供有关当前产品名称和版本的信息。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


提供有关当前产品名称和版本的信息。欲了解更多，请访问[输出文档中包含的生成器或生产者名称](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/)文档文章。

```cpp
class BuildVersionInfo
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | 获取产品的完整名称。 |
| static [get_Version](./get_version/)() | 获取产品版本。 |

## 示例



展示如何显示已安装的 Aspose.Words 版本信息。
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
