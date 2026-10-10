---
title: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection 方法"
linktitle: "get_AutoNumberingDetection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection 方法。获取或设置一个布尔值，指示在加载文档时是否执行自动编号检测。默认值在 C++ 中为 true。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


获取或设置一个布尔值，指示在加载文档时是否执行自动编号检测。默认值为 **true**。

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## 示例



展示如何禁用自动编号检测。
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## 另见

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
