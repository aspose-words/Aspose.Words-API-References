---
title: "طريقة Aspose::Words::Vba::VbaProject::get_IsProtected"
linktitle: "get_IsProtected"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Vba::VbaProject::get_IsProtected. يوضح ما إذا كان VbaProject محميًا بكلمة مرور في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words.vba/vbaproject/get_isprotected/
---
## VbaProject::get_IsProtected method


يوضح ما إذا كان [VbaProject](../) محميًا بكلمة مرور.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsProtected()
```


## أمثلة



يوضح ما إذا كان [VbaProject](../) محميًا بكلمة مرور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Vba protected.docm");
ASSERT_TRUE(doc->get_VbaProject()->get_IsProtected());
```

## انظر أيضًا

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
