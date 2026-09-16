---
title: "Aspose::Words::Vba::VbaProject::get_IsProtected 方法"
linktitle: "get_IsProtected"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Vba::VbaProject::get_IsProtected 方法。显示 VbaProject 是否受密码保护（在 C++ 中）。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


显示 [VbaProject](../) 是否受密码保护。

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## 示例



显示 [VbaProject](../) 是否受密码保护。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## 另见

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
