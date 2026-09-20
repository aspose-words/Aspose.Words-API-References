---
title: "Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture 方法"
linktitle: "GetCulture"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture 方法。返回一个 CultureInfo 对象，用于在 C++ 中字段的更新期间。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


返回一个用于字段更新期间的 **CultureInfo** 对象。

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文化 | System::String | 请求用于正在更新的字段的文化名称。 |
| 字段 | System::SharedPtr\<Aspose::Words::Fields::Field\> | 正在更新的字段。 |

### ReturnValue

应在字段更新时使用的文化对象。

## 另见

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
