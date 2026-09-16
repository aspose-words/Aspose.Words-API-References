---
title: "Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider 方法"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider 方法。获取或设置一个提供程序，该程序返回针对每个特定字段的文化对象（在 C++ 中）。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


获取或设置一个提供程序，为每个特定字段返回特定的文化对象。

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## 备注


当 [FieldUpdateCultureSource](../get_fieldupdateculturesource/) 的值为 [FieldCode](../../fieldupdateculturesource/) 时，会请求该提供程序。

如果提供程序存在，则使用其返回的文化对象进行字段更新。否则，将使用系统文化。
## 另见

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
